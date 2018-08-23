---
title: IConverterSessionMIMEToMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MIMEToMAPI
api_type:
- COM
ms.assetid: ee190ba7-9e71-97e4-7bf1-7b97adc73eed
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 60a058cc119290a0e14a76c914ac6d5a2d7a693b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593015"
---
# <a name="iconvertersessionmimetomapi"></a>IConverterSession::MIMEToMAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Converte um fluxo MIME em uma mensagem MAPI.
  
```cpp
HRESULT IConverterSession:: MIMEToMAPI ( 
     LPSTREAM pstm, 
     LPMESSAGE pmsg, 
     LPCSTR pszSrcSrv, 
     ULONG ulFlags 
);
```

## <a name="parameters"></a>Parâmetros

 _pstm_
  
> [in] Interface [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) a um fluxo MIME. 
    
 _pmsg_
  
> [out] Ponteiro para a mensagem para carregar. Consulte mapidefs.h para a definição de tipo de **LPMESSAGE**.
    
 _pszSrcSrv_
  
> [in] Este valor deve ser **nula**.
    
 _ulFlags_
  
> [in] Este parâmetro identificará nenhuma ação especial a ser executada durante a conversão. Ele deve ser zero (0) se nenhuma ação específica deve ser tomada, ou uma combinação dos seguintes valores:
    
CCSF_EMBEDDED_MESSAGE
  
> Informações não enviados/enviadas é persistente no não enviadas X.
    
CCSF_SMTP
  
> O fluxo MIME é uma mensagem do Simple MAPI Transfer Protocol (SMTP).
    
CCSF_INCLUDE_BCC
  
> Os destinatários Cco do fluxo de MIME devem ser incluídos na mensagem de MAPI.
    
CCSF_USE_RTF
  
> O corpo de HTML do fluxo de MIME deve ser convertido para formato Rich Text (RTF) na mensagem de MAPI.
    
## <a name="return-value"></a>Valor retornado

E_INVALIDARG
  
> Indica que _pstm_ for **nula**, _pmsg_ é **Nulo**ou _ulFlags_ é inválido. 
    
## <a name="remarks"></a>Comentários

Se você especificou **CCSF_USE_RTF** como parte do _ulFlags_ e o armazenamento de mensagens de destino oferece suporte a HTML e RTF, a mensagem MAPI será convertida em HTML ou RTF. Se a mensagem é convertida em RTF, será compactado convertido no novo formato RTF, qualquer HTML será incorporada na sequência de RTF compactada e a cadeia de caracteres será contida a [Propriedade canônico de PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md).
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI usa MimeToMAPI para converter um arquivo EML em uma mensagem MAPI.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI usa MAPIToMIMEStm para converter uma mensagem MAPI em um arquivo EML.  <br/> |
   
## <a name="see-also"></a>Confira também



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)


[Constantes MAPI](mapi-constants.md)

