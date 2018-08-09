---
title: IMsgStoreSetReceiveFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.SetReceiveFolder
api_type:
- COM
ms.assetid: 469f0412-1343-47ce-b6e8-e0d5e56c29bb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c30c38e1dbc944fd3016badf2621aef5de1e08f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767519"
---
# <a name="imsgstoresetreceivefolder"></a>IMsgStore::SetReceiveFolder

  
  
**Aplica-se a**: Outlook 
  
Estabelece uma pasta como destino para mensagens recebidas de uma classe de mensagem específica.
  
```cpp
HRESULT SetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parâmetros

 _lpszMessageClass_
  
> [in] Um ponteiro para a classe de mensagem que deve ser associado a nova pasta de recebimento. Se o parâmetro _lpszMessageClass_ for definido como NULL ou como uma sequência vazia, **SetReceiveFolder** define o padrão receber pasta para o armazenamento de mensagens. 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla o tipo de texto nas cadeias de caracteres no passado. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> A cadeia de caracteres de classe de mensagem está no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, a cadeia de caracteres de classe de mensagem é no formato ANSI.
    
 _cbEntryID_
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada da pasta para estabelecer como a pasta de recebimento. Se o parâmetro _lpEntryID_ for definido como NULL, **SetReceiveFolder** substitui as atuais receber pasta com padrão do armazenamento de mensagens. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> Uma pasta de recebimento foi estabelecida com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMsgStore::SetReceiveFolder** define ou altera a pasta de recebimento para uma classe de mensagem específica. Com **SetReceiveFolder**, um cliente pode usando sucessivas chamadas, especificar um diferentes receber a pasta para cada classe de mensagem definidas ou especificar que as mensagens de entrada para várias classes de mensagem todos caminham na mesma pasta. Por exemplo, um cliente pode ter sua própria classe de mensagens chegarem na sua própria pasta. Um aplicativo de fax pode designar uma pasta em que o provedor de armazenamento coloca os faxes de entrada e outra pasta na qual o provedor coloca os faxes de entrada.
  
Se ocorrer um erro durante a chamada para **SetReceiveFolder**, a configuração da pasta de recebimento permanecerá inalterada. 
  
Se **SetReceiveFolder** altera a configuração da pasta de recebimento com _lpEntryID_ definido como NULL, indicando que a pasta de recebimento padrão deve ser definida, **SetReceiveFolder** Retorna S_OK, mesmo se não havia nenhuma configuração existente para o indicado classe de mensagem. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnSetReceiveFolder  <br/> |MFCMAPI usa o método **IMsgStore::SetReceiveFolder** para definir uma pasta como a pasta de recebimento de uma classe de mensagem específica.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

