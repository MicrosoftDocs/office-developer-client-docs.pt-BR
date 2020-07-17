---
title: IConverterSessionMIMEToMAPI
manager: soliver
ms.date: 09/06/2019
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MIMEToMAPI
api_type:
- COM
ms.assetid: ee190ba7-9e71-97e4-7bf1-7b97adc73eed
description: 'Última modificação: 06 de setembro de 2019'
ms.openlocfilehash: c9fcffa8ad4dc982e869f4ccd449e1377fb1ea57
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160283"
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
  
> no Interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) para um fluxo MIME. 
    
 _pmsg_
  
> no Ponteiro para a mensagem a ser carregada. O chamador deve fornecer uma mensagem para que a API seja preenchida, portanto, o objeto deve ir [in]. Consulte mapidefs. h para a definição de tipo de **lpMessage**.
    
 _pszSrcSrv_
  
> no Este valor deve ser **nulo**.
    
 _ulFlags_
  
> no Esse parâmetro identifica qualquer ação especial a ser tomada durante a conversão. Ele deve ser zero (0) se nenhuma ação específica for executada ou uma combinação dos seguintes valores:
    
CCSF_EMBEDDED_MESSAGE
  
> As informações enviadas/não enviadas são mantidas em X-não enviadas.
    
CCSF_SMTP
  
> O fluxo MIME é para uma mensagem SMTP (Simple Mail Transfer Protocol).
    
CCSF_INCLUDE_BCC
  
> Os destinatários Cco do fluxo MIME devem ser incluídos na mensagem MAPI.
    
CCSF_USE_RTF
  
> O corpo HTML do fluxo MIME deve ser convertido em Rich Text Format (RTF) na mensagem MAPI.

CCSF_GLOBAL_MESSAGE
> O conversor deve lidar com o fluxo MIME como uma mensagem internacional (EAI/RFC6530). Sem suporte no Outlook 2013.
    
## <a name="return-value"></a>Valor de retorno

E_INVALIDARG
  
> Indica que _pStm_ é **nulo**, _pMsg_ é **nulo**ou _parâmetroulflags_ é inválido. 
    
## <a name="remarks"></a>Comentários

Se você especificou **CCSF_USE_RTF** como parte do _parâmetroulflags_ e o repositório de mensagens de destino oferecer suporte a HTML e RTF, a mensagem MAPI será convertida em HTML ou RTF. Se a mensagem for convertida para RTF, o formato convertido será compactado RTF, qualquer HTML será incorporado na cadeia de caracteres RTF compactada, e a cadeia de caracteres será contida na [Propriedade canônica PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md).
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MapiMime. cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI usa MimeToMAPI para converter um arquivo EML em uma mensagem MAPI.  <br/> |
|MapiMime. cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI usa MAPIToMIMEStm para converter uma mensagem MAPI em um arquivo EML.  <br/> |
   
## <a name="see-also"></a>Confira também



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)


[Constantes de MAPI](mapi-constants.md)

