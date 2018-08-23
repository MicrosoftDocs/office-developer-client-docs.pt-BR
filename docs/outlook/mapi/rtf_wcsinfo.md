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
ms.openlocfilehash: 2dd9f002401f8de52a9ad187b7e5850d47caf8a7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587380"
---
# <a name="rtfwcsinfo"></a>RTF_WCSINFO

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Essa estrutura permite que você especifique informações para descompactar o corpo da mensagem em compactado Rich Text Format (RTF) e, opcionalmente, retornará o fluxo de corpo em seu formato nativo.
  
## <a name="quick-info"></a>Informações rápidas

```cpp
typedef struct { 
    ULONG size; 
    ULONG ulFlags; 
    ULONG ulInCodePage; 
    ULONG ulOutCodePage; 
} RTF_WCSINFO;

```

## <a name="members"></a>Members

 _size_
  
> O tamanho da estrutura **RTF_WCSINFO** em número de bytes. 
    
 _ulFlags_
  
> Esse é o bitmask dos sinalizadores de opção para a função [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) . Os sinalizadores de opção com suporte são: 
    
|||
|:-----|:-----|
|MAPI_MODIFY  <br/> |Isso indica se o cliente pretende gravar a interface de fluxo ajustado que será retornada.  <br/> |
|STORE_UNCOMPRESSED_RTF  <br/> |Isso indica se o RTF descompactado deveria ser gravado para o fluxo indicados pelo ponteiro _lpCompressedRTFStream_ da função [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) .  <br/> |
|MAPI_NATIVE_BODY  <br/> |Isso indica se o fluxo de descompactados também é convertido em corpo nativo antes de retornar o fluxo. Esse sinalizador não pode ser combinado com o sinalizador **MAPI_MODIFY** .  <br/> |
   
 _ulInCodePage_
  
> Esse é o valor de página de código da mensagem. Normalmente, esse valor é obtido da [Propriedade canônico de PidTagInternetCodepage](pidtaginternetcodepage-canonical-property.md) na mensagem. Esse valor é usado apenas quando o sinalizador **MAPI_NATIVE_BODY** é passado _ulFlags_. Caso contrário, este valor será ignorado.
    
 _ulOutCodePage_
  
> Esse é o valor de página de código do fluxo descompactado retornado desejado. Se isso for definido como um valor diferente de zero, a função [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) converte o fluxo para a página de código especificada. Se isso for definido como um valor de zero, MAPI decide qual página de código a ser usado. Esse valor é usado somente quando o sinalizador **MAPI_NATIVE_BODY** é transmitido em _ulFlags_e o formato do corpo não for RTF. Caso contrário, este valor será ignorado.
    
## <a name="see-also"></a>Confira também



[WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)

