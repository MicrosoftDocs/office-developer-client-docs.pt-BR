---
title: Recupere o corpo da mensagem em RTF compactado e converta em seu formato nativo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9408da71-4abf-60cf-5412-58c5ceeb2205
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: e1c9de77c6e9a48326ad6b8f40d7f7a20ca762b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426111"
---
# <a name="retrieve-body-of-message-in-compressed-rtf-and-convert-to-its-native-format"></a><span data-ttu-id="95e22-103">Recupere o corpo da mensagem em RTF compactado e converta em seu formato nativo</span><span class="sxs-lookup"><span data-stu-id="95e22-103">Retrieve body of message in compressed RTF and convert to its native format</span></span>

<span data-ttu-id="95e22-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95e22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95e22-105">Este exemplo de código no Microsoft C++ mostra como usar a função exportada Microsoft Outlook 2010 ou Microsoft Outlook 2013 [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) para acessar o corpo de uma mensagem encapsulada em RTF compactado e obter o corpo em seu formato nativo.</span><span class="sxs-lookup"><span data-stu-id="95e22-105">This code example in Microsoft C++ shows you how to use the exported Microsoft Outlook 2010 or Microsoft Outlook 2013 function [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) to access the body of a message that is encapsulated in compressed RTF, and to obtain the body in its native format.</span></span> 
  
```cpp
//These are definitions for the WrapCompressedRTFStreamEx function. 
typedef HRESULT (STDMETHODCALLTYPE WRAPCOMPRESSEDRTFSTREAMEX) ( 
    LPSTREAM lpCompressedRTFStream, CONST RTF_WCSINFO * pWCSInfo, LPSTREAM * lppUncompressedRTFStream, RTF_WCSRETINFO * pRetInfo); 
typedef WRAPCOMPRESSEDRTFSTREAMEX *LPWRAPCOMPRESSEDRTFSTREAMEX; 
 
HRESULT TestWrapCompressedRTFStreamEx(LPMESSAGE lpMsg) 
{ 
    HRESULT         hRes = S_OK; 
    LPSTREAM        lpCompressed = NULL; 
    LPSTREAM        lpUncompressed = NULL; 
    char            szBody[1024] = {0}; 
    ULONG           ulRead = 0; 
    RTF_WCSINFO     wcsinfo = {0}; 
    RTF_WCSRETINFO  retinfo = {0}; 
    LPSPropValue    lpPropCPID = NULL; 
 
    retinfo.size = sizeof(RTF_WCSRETINFO); 
 
    wcsinfo.size = sizeof(RTF_WCSINFO); 
    wcsinfo.ulFlags = MAPI_NATIVE_BODY; 
    wcsinfo.ulOutCodePage = 0; 
 
    // Retrieve the value of the Internet code page. 
    // Pass this value to the WrapCompressedRTFStreamEx function. 
    // If the property is not found, the default is 0. 
    if(SUCCEEDED(hRes = HrGetOneProp(lpMsg, PR_INTERNET_CPID, &lpPropCPID))) 
    { 
        wcsinfo.ulInCodePage = lpPropCPID->Value.l; 
    } 
 
    // Open the compressed RTF stream. 
    if(SUCCEEDED(hRes = lpMsg->OpenProperty(PR_RTF_COMPRESSED, 
                                         &IID_IStream, 
                                         STGM_READ | STGM_DIRECT, 
                                         0, 
                                         (LPUNKNOWN*)&lpCompressed))) 
    { 
 
        // Notice that the WrapCompressedRTFStreamEx function has been loaded 
        // by using the GetProcAddress function into pfnWrapEx. 
 
        // Call the WrapCompressedRTFStreamEx function. 
        if(SUCCEEDED(hRes = pfnWrapEx(lpCompressed, 
                                   &wcsinfo, 
                                   &lpUncompressed, 
                                   &retinfo))) 
        { 
 
            printf("Body's native type is: "); 
 
            // Check what the native body type is. 
            switch(retinfo.ulStreamFlags) 
            { 
            case MAPI_NATIVE_BODY_TYPE_RTF: 
                printf("MAPI_NATIVE_BODY_TYPE_RTF\n"); 
                break; 
            case MAPI_NATIVE_BODY_TYPE_HTML: 
                printf("MAPI_NATIVE_BODY_TYPE_HTML\n"); 
                break; 
            case MAPI_NATIVE_BODY_TYPE_PLAINTEXT: 
                printf("MAPI_NATIVE_BODY_TYPE_PLAINTEXT\n"); 
                break; 
            default: 
                printf("UNKNOWN\n"); 
            } 
 
            // Read the first 1,000 characters out of the stream. 
            if(SUCCEEDED(hRes = lpUncompressed->Read(szBody, 1024, &ulRead))) 
            { 
                printf("First %d characters of the native body stream:\n%s\n", ulRead, szBody); 
            } 
        } 
    } 
 
    MAPIFreeBuffer(lpPropCPID); 
    if(lpUncompressed)lpUncompressed->Release(); 
    if(lpCompressed)lpCompressed->Release(); 
 
    return hRes; 
} 

```


