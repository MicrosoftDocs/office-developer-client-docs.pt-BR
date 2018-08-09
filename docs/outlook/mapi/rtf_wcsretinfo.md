---
title: RTF_WCSRETINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62561d8d-33cb-e482-7fa0-132afe2b464a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3a38a4604230c0aa3f5b0d104ae3b838f544b31d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770280"
---
# <a name="rtfwcsretinfo"></a>RTF_WCSRETINFO

**Aplica-se a**: Outlook 
  
Essa estrutura fornece informações sobre um fluxo no formato nativo retornado da descompactando o corpo de uma mensagem que é encapsulado no compactado Rich Text Format (RTF).
  
## <a name="quick-info"></a>Informações rápidas

```cpp
typedef struct { 
    ULONG size;    
    ULONG ulStreamFlags; 
} RTF_WCSRETINFO;
```

## <a name="members"></a>Members

_size_
  
> O tamanho da estrutura **RTF_WCSRETINFO** em número de bytes. 
    
_ulStreamFlags_
  
> Este é um valor que indica o formato do corpo da nativo. Este valor só será válido se o sinalizador **MAPI_NATIVE_BODY** é passado no parâmetro _ulFlags_ da estrutura [RTF_WCSINFO](rtf_wcsinfo.md) que é passado para a função [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) . Isso pode ser um dos seguintes valores: 
    
|||
|:-----|:-----|
|MAPI_NATIVE_BODY_TYPE_RTF  <br/> |Esse valor é usado apenas se _ulFlags_ inclui o sinalizador **MAPI_NATIVE_BODY** e corpo for RTF.  <br/> |
|MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT  <br/> |Esse valor é usado apenas se _ulFlags_ inclui o sinalizador **MAPI_NATIVE_BODY** e o corpo é o formato de texto sem formatação.  <br/> |
|MAPI_NATIVE_BODY_TYPE_HTML  <br/> |Esse valor é usado apenas se _ulFlags_ inclui o sinalizador **MAPI_NATIVE_BODY** e o corpo é o formato de linguagem de marcação de hipertexto (HTML).  <br/> |
   
## <a name="see-also"></a>Confira também

- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)

