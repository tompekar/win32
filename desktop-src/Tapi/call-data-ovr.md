---
Description: Call data is a variably sized buffer that can be used to accumulate information about a communications session. This information becomes available to all applications that own or monitor the session.
ms.assetid: 8b7a674f-ba78-4830-bb20-7fa74e202a1a
title: Call Data
ms.topic: article
ms.date: 05/31/2018
---

# Call Data

Call data is a variably sized buffer that can be used to accumulate information about a communications session. This information becomes available to all applications that own or monitor the session.

For example, the initial handler of an incoming session might request and enter client account information into a call data buffer, and then subsequent handlers would not have to repeat the request.

Not all service providers support use of this information.

**TAPI 2.x:** See [**lineGetCallInfo**](https://msdn.microsoft.com/library/ms735720(v=VS.85).aspx), [**lineSetCallData**](https://msdn.microsoft.com/library/ms736084(v=VS.85).aspx) (**dwCallDataSize** and **dwCallDataOffset** members of [**LINECALLINFO**](https://msdn.microsoft.com/library/ms735527(v=VS.85).aspx)), [**LINE\_CALLINFO**](https://msdn.microsoft.com/library/ms736518(v=VS.85).aspx) message (*dwParam1* set to LINECALLINFOSTATE\_CALLDATA).

**TAPI 3.x:** See [**ITCallInfo::put\_CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfobuffer) (**CIB\_CALLDATABUFFER** member of [**CALLINFO\_BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)); [**ITCallInfoChangeEvent::get\_Cause**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) returns the **CIC\_CALLDATA** member of [**CALLINFOCHANGE\_CAUSE**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause).

 

 



