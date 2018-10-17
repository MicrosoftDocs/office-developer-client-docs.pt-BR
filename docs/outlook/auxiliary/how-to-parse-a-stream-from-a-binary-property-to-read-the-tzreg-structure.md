---
title: Analisar um fluxo de uma propriedade binária para ler a estrutura TZREG
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 9e36e0d9-a28b-5978-0e23-f76e1bf506b5
description: Este tópico mostra como ler a estrutura TZREG do formato persistente armazenado na propriedade binária PidLidTimeZoneStruct.
ms.openlocfilehash: f59251ebc980ca10f4ddce76b34e700bc430540a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387395"
---
# <a name="parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure"></a><span data-ttu-id="ee5d2-103">Analisar um fluxo de uma propriedade binária para ler a estrutura TZREG</span><span class="sxs-lookup"><span data-stu-id="ee5d2-103">Parse a stream from a binary property to read the TZREG structure</span></span>

<span data-ttu-id="ee5d2-104">Este tópico mostra como ler a estrutura [TZREG](tzreg.md) do formato persistente armazenado na propriedade binária [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="ee5d2-104">This topic shows how to read the [TZREG](tzreg.md) structure from the persisted format stored in the binary property [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx).</span></span>
  
```cpp
TZREG* BinToTZREG(ULONG cbReg, LPBYTE lpbReg)  
{ 
    if (!lpbReg) return NULL;  
 
    // Update this if parsing code is changed. 
    if (cbReg &amp;lt; 3*sizeof(long) + 2*sizeof(WORD) + 2*sizeof(SYSTEMTIME)) return NULL; 
 
    TZREG tzReg = {0}; 
    LPBYTE lpPtr = lpbReg; 
 
    tzReg.lBias = *((long*)lpPtr); 
    lpPtr += sizeof(long); 
    tzReg.lStandardBias = *((long*)lpPtr); 
    lpPtr += sizeof(long); 
    tzReg.lDaylightBias = *((long*)lpPtr); 
    lpPtr += sizeof(long); 
    lpPtr += sizeof(WORD);// reserved 
 
    tzReg.stStandardDate = *((SYSTEMTIME*)lpPtr); 
    lpPtr += sizeof(SYSTEMTIME); 
    lpPtr += sizeof(WORD);// reserved 
    tzReg.stDaylightDate = *((SYSTEMTIME*)lpPtr); 
    lpPtr += sizeof(SYSTEMTIME); 
 
    TZREG* ptzReg = NULL; 
    ptzReg = new TZREG; 
    if (ptzReg) 
    { 
        *ptzReg = tzReg; 
    } 
 
    return ptzReg; 
} 

```

## <a name="see-also"></a><span data-ttu-id="ee5d2-105">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee5d2-105">See also</span></span>

- [<span data-ttu-id="ee5d2-106">Ler propriedades de fuso horário de um compromisso</span><span class="sxs-lookup"><span data-stu-id="ee5d2-106">Read time zone properties from an appointment</span></span>](how-to-read-time-zone-properties-from-an-appointment.md)

