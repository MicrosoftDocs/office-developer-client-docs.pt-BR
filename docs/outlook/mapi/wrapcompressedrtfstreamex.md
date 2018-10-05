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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391728"
---
# <a name="wrapcompressedrtfstreamex"></a>WrapCompressedRTFStreamEx

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descompacta o corpo de uma mensagem de email que está no compactado Rich Text Format (RTF), indica o formato do fluxo descompactado, opcionalmente converte o fluxo descompactado em seu formato nativo e retorna o fluxo de descompactados ou o convertido stream nativo.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Exportá-los por:  <br/> |Msmapi32  <br/> |
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
  
> [in] Este é um ponteiro para um fluxo que é aberto na [Propriedade canônico de PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) de uma mensagem. 
    
_pWCSInfo_
  
> [in] Este é um ponteiro para um 
    
   Estrutura [RTF_WCSINFO](rtf_wcsinfo.md) que contém opções para a função. 
    
_lppUncompressedRTFStream_
  
> [out] Este é um ponteiro para o local onde um stream para o RTF descompactado é retornado. 
    
_pRetInfo_
  
> [out] Este é um ponteiro para uma estrutura [RTF_WCSRETINFO](rtf_wcsretinfo.md) que contém informações sobre o formato do fluxo retornado descompactado. 
    
## <a name="return-values"></a>Valores de retorno

S_OK 
  
- A chamada de função é bem-sucedida.
    
MAPI_E_INVALID_PARAMETER 
  
- Isso será retornado se o sinalizador **MAPI_NATIVE_BODY** é combinado com o sinalizador **MAPI_MODIFY** no campo **ulFlags** da estrutura **RTF_WCSINFO** apontado por *pWCSInfo* . 
    
## <a name="remarks"></a>Comentários

**WrapCompressedRTFStreamEx** permite que você acesse o corpo de uma mensagem de email encapsulado em RTF compactado, descompactando o fluxo, retorna stream descompactado e seu formato e, opcionalmente, o fluxo de corpo nativo. O fluxo de corpo nativo pode estar em RTF, HTML ou texto sem formatação. 
  
O modelo de objeto do Microsoft Office Outlook fornece uma propriedade de **corpo** de uma [Propriedade MailItem BodyFormat (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) que indica o formato do corpo de texto e objetos de **MailItem** . Por design, uma solução que não é confiável pelo Outlook invoca caixas de diálogo de segurança geradas pelo protetor de segurança do Outlook. Usando a função MAPI exportada **WrapCompressedRTFStreamEx** permite que uma solução para usar MAPI em vez de modelo de objeto do Outlook e evitar essas caixas de diálogo de segurança. 
  
Porque o **MAPI\_NATIVE_BODY** sinalizador não pode ser combinado com o **MAPI\_modificar** sinalizador no campo **ulFlags** do **RTF\_WCSINFO** estrutura apontado pela *pWCSInfo*, você só poderá acessar o nativo fluxo do corpo em modo somente leitura. Para acessar o fluxo de corpo nativos no modo leitura/gravação, você deve usar a função **WrapCompressedRTFStream** . 
  
## <a name="see-also"></a>Confira também

- [Recuperar o corpo de uma mensagem em RTF compactado e convertê-lo ao formato nativo](how-to-retrieve-the-body-of-a-message-in-compressed-rtf-and-convert.md)

