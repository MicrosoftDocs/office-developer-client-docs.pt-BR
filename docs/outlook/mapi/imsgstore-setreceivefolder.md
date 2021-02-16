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
ms.openlocfilehash: efa5d60098fd5f16328669249a8445a124d9878b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434085"
---
# <a name="imsgstoresetreceivefolder"></a>IMsgStore::SetReceiveFolder

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Estabelece uma pasta como o destino para mensagens de entrada de uma classe de mensagem específica.
  
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
  
> [in] Um ponteiro para a classe de mensagem que deve ser associada à nova pasta de recebimento. Se o  _parâmetro lpszMessageClass_ for definido como NULL ou uma cadeia de caracteres vazia, **SetReceiveFolder** definirá a pasta de recebimento padrão para o armazenamento de mensagens. 
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla o tipo do texto nas cadeias de caracteres passadas. O sinalizador a seguir pode ser definido:
    
MAPI_UNICODE 
  
> A cadeia de caracteres de classe de mensagem está no formato Unicode. Se o MAPI_UNICODE não estiver definido, a cadeia de caracteres da classe de mensagem está no formato ANSI.
    
 _cbEntryID_
  
> [in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada da pasta para estabelecer como a pasta de recebimento. Se o  _parâmetro lpEntryID_ for definido como NULL, **SetReceiveFolder** substituirá a pasta de recebimento atual pelo padrão do armazenamento de mensagens. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> Uma pasta de recebimento foi estabelecida com êxito.
    
## <a name="remarks"></a>Comentários

O **método IMsgStore::SetReceiveFolder** define ou altera a pasta de recebimento de uma classe de mensagem específica. Com **SetReceiveFolder**, um cliente pode, usando chamadas sucessivas, especificar uma pasta de recebimento diferente para cada classe de mensagem definida ou especificar que as mensagens de entrada para várias classes de mensagens vão para a mesma pasta. Por exemplo, um cliente pode ter sua própria classe de mensagens chegar em sua própria pasta. Um aplicativo de fax pode designar uma pasta na qual o provedor de armazenamento coloca faxes de entrada e outra pasta na qual o provedor coloca faxes de saída.
  
Se ocorrer um erro durante a chamada para **SetReceiveFolder,** a configuração da pasta de recebimento permanecerá inalterada. 
  
Se **SetReceiveFolder** mudar a configuração da pasta de recebimento com  _lpEntryID_ definido como NULL, indicando que a pasta de recebimento padrão deve ser definida, **SetReceiveFolder** retornará S_OK mesmo se não houver nenhuma configuração existente para a classe de mensagem indicada. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnSetReceiveFolder  <br/> |MFCMAPI usa o método **IMsgStore::SetReceiveFolder** para definir uma pasta como a pasta de recebimento para uma classe de mensagem específica.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

