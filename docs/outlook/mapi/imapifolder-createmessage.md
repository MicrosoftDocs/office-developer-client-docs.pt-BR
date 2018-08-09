---
title: IMAPIFolderCreateMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CreateMessage
api_type:
- COM
ms.assetid: e0222afa-c148-4735-a603-cac7be6c91f9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8d7e6dfbf9e6a751845adb2319b66462bcde651f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766964"
---
# <a name="imapifoldercreatemessage"></a>IMAPIFolder::CreateMessage

  
  
**Aplica-se a**: Outlook 
  
Cria uma nova mensagem.
  
```cpp
HRESULT CreateMessage(
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMessage
);
```

## <a name="parameters"></a>Parâmetros

 _lpInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) que representa a interface para ser usado para acessar a nova mensagem. Identificadores de interface válidos incluem IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer e IID_IMAPIFolder. Passar NULL faz com que o provedor de armazenamento de mensagem retornar a interface de mensagem padrão, [IMessage: IMAPIProp](imessageimapiprop.md). 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como a mensagem é criada. Sinalizadores a seguir podem ser definidos:
    
ITEMPROC_FORCE
  
> Indica para o repositório de pasta particular (. PST) que a mensagem é qualificada para regras de processamento antes que o repositório notificará qualquer cliente escuta a partir da chegada da nova mensagem. Processamento apenas das regras se aplica às novas mensagens que são criadas em um servidor que não seja um Microsoft Exchange Server, pois o Exchange Server processa as regras para mensagens no servidor. Portanto, o provedor ou criar a mensagem de cliente deve passar por esse sinalizador em combinação com o salvamento de uma mensagem com [IMAPIPProp::SaveChanges](imapiprop-savechanges.md) usando NON_EMS_XP_SAVE, que indica que o servidor não é um servidor Exchange. 
    
MAPI_ASSOCIATED 
  
> A mensagem a ser criado deve ser incluída na tabela de conteúdo associado no lugar do índice de conteúdo padrão. Mensagens associadas estão ocultos na interação do usuário.
    
MAPI_DEFERRED_ERRORS 
  
> **CreateMessage** é permitido tenha êxito, mesmo se a operação de criação não foi totalmente concluída. Isso significa que a nova mensagem pode não estar disponível imediatamente ao chamador. 
    
 _lppMessage_
  
> [out] Um ponteiro para um ponteiro para a mensagem recém-criado.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A mensagem foi criada com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPIFolder::CreateMessage** cria uma nova mensagem com conteúdo genérico ou associado e atribui um identificador de entrada. O identificador de entrada consiste em uma parte que representa o provedor de armazenamento de mensagem e uma parte que representa a mensagem individual. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Você pode escolher se deseja definir todas as propriedades de mensagem necessária no **CreateMessage** ou no método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) da mensagem. Você não precisará disponibilizar essas propriedades até que uma gravação bem-sucedida tenha ocorrido. 
  
Para obter mais informações sobre como trabalhar com informações associadas, consulte [Folder-Associated tabelas de informações](folder-associated-information-tables.md) e [Conteúdo](contents-tables.md). 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Alguns provedores de repositório de mensagem permitem o identificador de entrada da nova mensagem estejam disponíveis imediatamente após **CreateMessage** retorna; outros provedores de armazenamento de mensagem atrasam a sua disponibilidade até que a mensagem será salva. Porque nem todos os provedores de armazenamento de mensagem geram um identificador de entrada para uma nova mensagem, até que você tenha chamado o método de **IMAPIProp::SaveChanges** da mensagem, você pode ser capaz de acessar o identificador de entrada quando **CreateMessage** retorna. Além disso, a nova mensagem pode não ser incluída na tabela de conteúdo da pasta até que ocorra a salvar. 
  
Espere o identificador de entrada atribuído à nova mensagem ser exclusivas não apenas no armazenamento da mensagem atual, mas bem provável em todos os repositórios de mensagem que estão abertos ao mesmo tempo. Uma exceção a essa regra ocorre quando várias entradas para um armazenamento de mensagens aparecem no perfil. Isso faz com que o armazenamento de mensagens a serem abertas várias vezes e os identificadores de entrada a ser duplicado. 
  
Para criar uma mensagem de saída, chame o método de **IMAPIFolder::CreateMessage** da pasta caixa de saída. 
  
Se você excluir uma pasta que contém uma nova mensagem antes que a mensagem será salva, os resultados são indefinidos.
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolder::OnNewMessage  <br/> |MFCMAPI usa o método **IMAPIFolder::CreateMessage** para criar e salvar uma nova mensagem.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

