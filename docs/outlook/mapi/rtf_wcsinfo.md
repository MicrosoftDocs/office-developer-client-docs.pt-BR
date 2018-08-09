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
ms.openlocfilehash: c328e79b7e474369f11f8a4002e00137659db3c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770298"
---
# <a name="rtfwcsinfo"></a>RTF_WCSINFO

  
  
**Aplica-se a**: Outlook 
  
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

