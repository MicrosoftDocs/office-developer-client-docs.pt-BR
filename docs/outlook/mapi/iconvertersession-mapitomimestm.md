---
title: IConverterSessionMAPIToMIMEStm
ms.date: 9/20/2017
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MAPIToMIMEStm
api_type:
- COM
ms.assetid: 8660c701-f7f4-8d92-7984-5dae7f677783
description: 'Modificado pela última vez: 20 de setembro de 2017'
ms.openlocfilehash: b59114926d44ba613efbbde1c8dd5d17c26756c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766899"
---
# <a name="iconvertersessionmapitomimestm"></a>IConverterSession::MAPIToMIMEStm
 
  
**Aplica-se a**: Outlook 
  
Converte uma mensagem MAPI em um fluxo MIME.
  
```cpp
HRESULT IConverterSession::MAPIToMIMEStm( 
    LPMESSAGE pmsg, 
    LPSTREAM pstm, 
    ULONG ulFlags 
);
```

## <a name="parameters"></a>Parâmetros

 _pmsg_
  
> [in] Ponteiro para a mensagem para converter. Consulte mapidefs.h para a definição de tipo de **LPMESSAGE**.
    
 _pstm_
  
> [out] Interface [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) para o fluxo de saída. 
    
 _ulFlags_
  
>  [in] Sinalizadores que indicam ações específicas para o conversor: 
    
CCSF_8BITHEADERS
  
> O conversor deve permitir que os cabeçalhos de 8 bits.
    
CCSF_EMBEDDED_MESSAGE
  
> Informações não enviados/enviadas é persistente no não enviadas X.
    
CCSF_GLOBAL_MESSAGE
  
> O conversor deve criar uma mensagem internacional (EAI/RFC6530).
    
CCSF_INCLUDE_BCC
  
> Os destinatários Cco da mensagem MAPI devem ser incluídos no fluxo de MIME.
    
CCSF_NO_MSGID
  
> Não inclua o campo de Id de mensagem em mensagens de saída.
    
CCSF_NOHEADERS
  
> O conversor deve ignorar os cabeçalhos da mensagem externo.
    
CCSF_PLAIN_TEXT_ONLY
  
> O conversor apenas deve enviar texto sem formatação.
    
CCSF_SMTP
  
> O conversor está sendo passado como uma mensagem SMTP. Esse sinalizador sempre deve ser definido.
    
CCSF_USE_RTF
  
> O conversor deve converter de HTML para o formato RTF na mensagem MIME.
    
CCSF_USE_TNEF
  
> O conversor deve usar o formato TNEF Transport Neutral Encapsulation Format () na mensagem MIME.
    
## <a name="return-values"></a>Valores de retorno

E_INVALIDARG
  
> Sinalizadores inválidos foram passados ou *pmsg* ou *pstm* é nulo. 
    
## <a name="remarks"></a>Comentários

Suporte apenas para os tipos de mensagem padrão do Outlook.
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI usa MimeToMAPI para converter um arquivo EML em uma mensagem MAPI.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI usa MAPIToMIMEStm para converter uma mensagem MAPI em um arquivo EML.  <br/> |
   
## <a name="see-also"></a>Confira também



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)
  
[Propriedade canônica PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)
  
[Propriedade can�nico de PidLidUseTnef](pidlidusetnef-canonical-property.md)


[Constantes MAPI](mapi-constants.md)

