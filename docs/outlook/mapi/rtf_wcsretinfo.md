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
ms.openlocfilehash: cfa18c215fc98610b836db31e2a07581291910be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426167"
---
# <a name="rtfwcsretinfo"></a>RTF_WCSRETINFO

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Essa estrutura fornece informações sobre um fluxo no formato nativo retornado da descompactação do corpo de uma mensagem encapsulada em formato Rich Text (RTF) compactado.
  
## <a name="quick-info"></a>Informações rápidas

```cpp
typedef struct { 
    ULONG size;    
    ULONG ulStreamFlags; 
} RTF_WCSRETINFO;
```

## <a name="members"></a>Membros

_size_
  
> O tamanho da estrutura **RTF_WCSRETINFO** em número de bytes. 
    
_ulStreamFlags_
  
> Este é um valor que indica o formato do corpo nativo. Esse valor só será válido se o sinalizador **MAPI_NATIVE_BODY** for passado no parâmetro _Parâmetroulflags_ da estrutura [RTF_WCSINFO](rtf_wcsinfo.md) que é passada para a função [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) . Pode ser um dos seguintes valores: 
    
|||
|:-----|:-----|
|MAPI_NATIVE_BODY_TYPE_RTF  <br/> |Esse valor só será usado se _parâmetroulflags_ incluir o sinalizador **MAPI_NATIVE_BODY** e o corpo for RTF.  <br/> |
|MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT  <br/> |Esse valor é usado somente se _parâmetroulflags_ inclui o sinalizador **MAPI_NATIVE_BODY** e o corpo é o formato de texto sem formatação.  <br/> |
|MAPI_NATIVE_BODY_TYPE_HTML  <br/> |Esse valor é usado somente se _parâmetroulflags_ inclui o sinalizador **MAPI_NATIVE_BODY** e o corpo é o formato HTML (Hypertext Markup Language).  <br/> |
   
## <a name="see-also"></a>Confira também

- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)

