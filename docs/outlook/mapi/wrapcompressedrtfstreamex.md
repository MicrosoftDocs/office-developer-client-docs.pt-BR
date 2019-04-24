---
title: WrapCompressedRTFStreamEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 45abee1c-d7fb-b0f9-522d-8ba34caf1094
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: af176c0ce327e6498a5d07f6d902c50f7323f813
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325771"
---
# <a name="wrapcompressedrtfstreamex"></a>WrapCompressedRTFStreamEx

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descompacta o corpo de uma mensagem de email que está no formato Rich Text (RTF), indica o formato do fluxo descompactado, converte opcionalmente o fluxo descompactado em seu formato nativo e retorna o fluxo descompactado ou o fluxo nativo convertido.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Exportado por:  <br/> |msmapi32.dll  <br/> |
|Chamado por:  <br/> |Cliente  <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
   
```cpp
HRESULT __stdcall WrapCompressedRTFStreamEx( 
    LPSTREAM            lpCompressedRTFStream, 
    CONST RTF_WCSINFO   *pWCSInfo, 
    LPSTREAM            *lppUncompressedRTFStream, 
    RTF_WCSRETINFO      *pRetInfo); 

```

## <a name="parameters"></a>Parâmetros

_lpCompressedRTFStream_
  
> no Este é um ponteiro para um Stream que é aberto na [Propriedade canônica PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) de uma mensagem. 
    
_pWCSInfo_
  
> no Este é um ponteiro para um 
    
   Estrutura [RTF_WCSINFO](rtf_wcsinfo.md) que contém opções para a função. 
    
_lppUncompressedRTFStream_
  
> bota Este é um ponteiro para o local onde um Stream para o RTF descompactado é retornado. 
    
_pRetInfo_
  
> bota Este é um ponteiro para uma estrutura [RTF_WCSRETINFO](rtf_wcsretinfo.md) que contém informações sobre o formato do fluxo descompactado retornado. 
    
## <a name="return-values"></a>Valor de retorno

S_OK 
  
- A chamada de função foi bem-sucedida.
    
MAPI_E_INVALID_PARAMETER 
  
- Isso é retornado se o sinalizador **MAPI_NATIVE_BODY** é combinado com o sinalizador **MAPI_MODIFY** no campo **parâmetroulflags** da estrutura **RTF_WCSINFO** indicada por *pWCSInfo* . 
    
## <a name="remarks"></a>Comentários

O **WrapCompressedRTFStreamEx** permite que você acesse o corpo de uma mensagem de email encapsulada no rtf compactado descompactando o fluxo, retorna o fluxo descompactado e seu formato e, opcionalmente, o fluxo de corpo nativo. O fluxo de corpo nativo pode estar em RTF, texto sem formatação ou HTML. 
  
O modelo de objeto do Microsoft Office Outlook fornece uma propriedade **Body** para objetos **MailItem** e uma [Propriedade MailItem. BodyFormat (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) que indica o formato do corpo de texto. Por design, uma solução que não é confiável para o Outlook invoca as caixas de diálogo de segurança geradas pelo proteção de segurança do Outlook. Usando a função MAPI exportada **WrapCompressedRTFStreamEx** permite que uma solução use MAPI em vez do modelo de objeto do Outlook e evite essas caixas de diálogo de segurança. 
  
Como o **sinalizador\_MAPI NATIVE_BODY** não pode ser combinado com o sinalizador de **modificação\_MAPI** no campo **parâmetroulflags** da **estrutura\_RTF WCSINFO** indicada por *pWCSInfo*, você só pode acessar o nativo fluxo de corpo no modo somente leitura. Para acessar o fluxo de corpo nativo no modo de leitura/gravação, você deve usar a função **WrapCompressedRTFStream** . 
  
## <a name="see-also"></a>Confira também

- [Recuperar o corpo de uma mensagem em RTF compactado e conVertê-lo em seu formato nativo](how-to-retrieve-the-body-of-a-message-in-compressed-rtf-and-convert.md)

