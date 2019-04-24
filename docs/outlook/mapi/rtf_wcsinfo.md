---
title: RTF_WCSINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0c94501e-0ec7-e836-33a7-adcf5a61b375
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6bec29aa0e88e0224f9cd6049553f2df6379e23d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344643"
---
# <a name="rtfwcsinfo"></a>RTF_WCSINFO

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Essa estrutura permite que você especifique informações para descompactar o corpo de uma mensagem no formato Rich Text (RTF) compactado e, opcionalmente, retornar o fluxo do corpo em seu formato nativo.
  
## <a name="quick-info"></a>Informações rápidas

```cpp
typedef struct { 
    ULONG size; 
    ULONG ulFlags; 
    ULONG ulInCodePage; 
    ULONG ulOutCodePage; 
} RTF_WCSINFO;

```

## <a name="members"></a>Membros

 _size_
  
> O tamanho da estrutura **RTF_WCSINFO** em número de bytes. 
    
 _ulFlags_
  
> Esta é a bitmask dos sinalizadores de opção para a função [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) . Os sinalizadores de opção com suporte são: 
    
|||
|:-----|:-----|
|MAPI_MODIFY  <br/> |Isso indica se o cliente pretende gravar a interface de fluxo encapsulada retornada.  <br/> |
|STORE_UNCOMPRESSED_RTF  <br/> |Isso indica se o RTF descompactado deve ser gravado no fluxo que é apontado pelo ponteiro _lpCompressedRTFStream_ da função [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) .  <br/> |
|MAPI_NATIVE_BODY  <br/> |Isso indica se o fluxo descompactado também é convertido no corpo nativo antes de retornar o fluxo. Este sinalizador não pode ser combinado com o sinalizador **MAPI_MODIFY** .  <br/> |
   
 _ulInCodePage_
  
> Este é o valor da página de código da mensagem. Normalmente, esse valor é obtido da [Propriedade canônica PidTagInternetCodepage](pidtaginternetcodepage-canonical-property.md) na mensagem. Esse valor é usado apenas quando o sinalizador **MAPI_NATIVE_BODY** é passado em _parâmetroulflags_. Caso contrário, esse valor será ignorado.
    
 _ulOutCodePage_
  
> Este é o valor da página de código do Stream descompactado retornado que você deseja. Se for definido como um valor diferente de zero, a função [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) converte o Stream na página de código especificada. Se for definido como um valor zero, MAPI decide qual página de código usar. Esse valor é usado somente quando o sinalizador **MAPI_NATIVE_BODY** é passado em _parâmetroulflags_, e o formato do corpo não é RTF. Caso contrário, esse valor será ignorado.
    
## <a name="see-also"></a>Confira também



[WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)

