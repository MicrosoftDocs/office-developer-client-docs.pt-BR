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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430529"
---
# <a name="rtf_wcsinfo"></a>RTF_WCSINFO

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Essa estrutura permite especificar informações para descompactar o corpo de uma mensagem em RTF (Formato Rich Text) compactado e, opcionalmente, retornar o fluxo de corpo em seu formato nativo.
  
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
  
> Esta é a máscara de bits dos sinalizadores de opção para [a função WrapCompressedRTFStreamEx.](wrapcompressedrtfstreamex.md) Os sinalizadores de opção com suporte são: 
    
|||
|:-----|:-----|
|MAPI_MODIFY  <br/> |Isso indica se o cliente pretende gravar a interface de fluxo envolvida que é retornada.  <br/> |
|STORE_UNCOMPRESSED_RTF  <br/> |Isso indica se o RTF descompactado deve ser gravado no fluxo apontado pelo ponteiro _lpCompressedRTFStream_ da função [WrapCompressedRTFStreamEx.](wrapcompressedrtfstreamex.md)  <br/> |
|MAPI_NATIVE_BODY  <br/> |Isso indica se o fluxo descompactado também é convertido no corpo nativo antes de retornar o fluxo. Esse sinalizador não pode ser combinado com o **MAPI_MODIFY** sinalizador.  <br/> |
   
 _ulInCodePage_
  
> Este é o valor da página de código da mensagem. Normalmente, esse valor é obtido da propriedade canônica [PidTagInternetCodepage](pidtaginternetcodepage-canonical-property.md) na mensagem. Esse valor só é usado quando o **MAPI_NATIVE_BODY** sinalizador é passado  _em ulFlags_. Caso contrário, esse valor será ignorado.
    
 _ulOutCodePage_
  
> Esse é o valor de página de código do fluxo descompactado retornado que você deseja. Se isso for definido como um valor não zero, a função [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) converterá o fluxo na página de código especificada. Se isso for definido como um valor zero, o MAPI decidirá qual página de código usar. Esse valor é usado somente quando o **MAPI_NATIVE_BODY** sinalizador é passado  _em ulFlags_ e o formato do corpo não é RTF. Caso contrário, esse valor será ignorado.
    
## <a name="see-also"></a>Confira também



[WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)

