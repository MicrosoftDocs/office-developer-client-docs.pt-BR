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
description: 'Última modificação: 20 de setembro de 2017'
ms.openlocfilehash: 55c547c4dae1acc3e9874edc7778f53a5d34f957
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326940"
---
# <a name="iconvertersessionmapitomimestm"></a>IConverterSession::MAPIToMIMEStm
 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Converte uma mensagem MAPI em um fluxo MIME.
  
```cpp
HRESULT IConverterSession::MAPIToMIMEStm( 
    LPMESSAGE pmsg, 
    LPSTREAM pstm, 
    ULONG ulFlags 
);
```

## <a name="parameters"></a>Parâmetros

 _pMsg_
  
> no Ponteiro para a mensagem a ser convertida. Consulte mapidefs. h para a definição de tipo de **lpMessage**.
    
 _pStm_
  
> bota Interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) para saída do Stream. 
    
 _ulFlags_
  
>  no Sinalizadores que indicam ações específicas para o conversor: 
    
CCSF_8BITHEADERS
  
> O conversor deve permitir cabeçalhos de 8 bits.
    
CCSF_EMBEDDED_MESSAGE
  
> As informações enviadas/não enviadas são mantidas em X-não enviadas.
    
CCSF_GLOBAL_MESSAGE
  
> O conversor deve criar uma mensagem internacional (EAI/RFC6530).
    
CCSF_INCLUDE_BCC
  
> Os destinatários Cco da mensagem MAPI devem ser incluídos no fluxo MIME.
    
CCSF_NO_MSGID
  
> Não inclua o campo Message-ID em mensagens de saída.
    
CCSF_NOHEADERS
  
> O conversor deve ignorar os cabeçalhos da mensagem externa.
    
CCSF_PLAIN_TEXT_ONLY
  
> O conversor deve apenas enviar texto sem formatação.
    
CCSF_SMTP
  
> O conversor é passado uma mensagem SMTP. Esse sinalizador deve sempre ser definido.
    
CCSF_USE_RTF
  
> O conversor deve converter HTML em formato RTF na mensagem MIME.
    
CCSF_USE_TNEF
  
> O conversor deve usar o formato TNEF (Transport neutral Encapsulation Format) na mensagem MIME.
    
## <a name="return-values"></a>Valor de retorno

E_INVALIDARG
  
> Sinalizadores inVálidos foram passados ou *pMsg* ou *pStm* é nulo. 
    
## <a name="remarks"></a>Comentários

Com suporte apenas para tipos de mensagem padrão do Outlook.
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MapiMime. cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI usa MimeToMAPI para converter um arquivo EML em uma mensagem MAPI.  <br/> |
|MapiMime. cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI usa MAPIToMIMEStm para converter uma mensagem MAPI em um arquivo EML.  <br/> |
   
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


[Constantes de MAPI](mapi-constants.md)

