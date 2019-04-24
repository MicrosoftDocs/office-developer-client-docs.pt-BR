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
ms.openlocfilehash: 4d38648f5e3084c8342fca8d18f0bd3efc915155
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280082"
---
# <a name="imapifoldercreatemessage"></a>IMAPIFolder::CreateMessage

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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
  
> no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar a nova mensagem. Os identificadores de interface válidos incluem IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer e IID_IMAPIFolder. Passar NULL faz com que o provedor de repositório de mensagens retorne a interface de mensagens padrão, [IMessage: IMAPIProp](imessageimapiprop.md). 
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como a mensagem é criada. Os seguintes sinalizadores podem ser definidos:
    
ITEMPROC_FORCE
  
> Indica o repositório de pastas pessoais (PST) que a mensagem está qualificada para o processamento de regras antes que o repositório Notifique qualquer cliente de escuta da chegada da nova mensagem. O processamento de regras só se aplica a novas mensagens criadas em um servidor que não seja do Microsoft Exchange Server, pois o Exchange Server processa as regras para mensagens no servidor. Portanto, o provedor ou o cliente que cria a mensagem deve passar esse sinalizador em combinação com o salvamento de uma mensagem com [IMAPIPProp:: SaveChanges](imapiprop-savechanges.md) usando NON_EMS_XP_SAVE, que indica que o servidor não é um servidor Exchange. 
    
MAPI_ASSOCIATED 
  
> A mensagem a ser criada deve ser incluída na tabela de conteúdo associado, em vez da tabela de conteúdo padrão. As mensagens associadas são ocultas da interação do usuário.
    
MAPI_DEFERRED_ERRORS 
  
> **CreateMessage** tem permissão para ter êxito, mesmo que a operação de criação não tenha sido totalmente concluída. Isso significa que a nova mensagem pode não estar imediatamente disponível para o chamador. 
    
 _lppMessage_
  
> bota Um ponteiro para um ponteiro para a mensagem recém-criada.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A mensagem foi criada com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPIFolder:: CreateMessage** cria uma nova mensagem com conteúdo genérico ou associado e atribui um identificador de entrada. O identificador de entrada consiste em uma parte que representa o provedor de armazenamento de mensagens e uma parte que representa a mensagem individual. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Você pode escolher se deseja definir todas as propriedades de mensagem necessárias em **CreateMessage** ou no método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) da mensagem. Você não precisa disponibilizar essas propriedades até que uma gravação bem-sucedida tenha ocorrido. 
  
Para obter mais informações sobre como trabalhar com informações associadas, confira tabelas [de informações associadas a pastas](folder-associated-information-tables.md) e [tabelas de conteúdo](contents-tables.md). 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Alguns provedores de repositórios de mensagens permitem que o identificador de entrada da nova mensagem fique **** disponível imediatamente após o retorno de CreateMessage; outros provedores de repositórios de mensagens atrasam sua disponibilidade até que a mensagem seja salva. Como nem todos os provedores de repositório de mensagens geram um identificador de entrada para uma nova mensagem até que você tenha chamado o método **IMAPIProp:: SaveChanges** da mensagem, talvez não seja possível **** acessar o identificador de entrada quando CreateMessage retornar. Além disso, a nova mensagem pode não ser incluída na tabela de conteúdo da pasta até que o salvamento ocorra. 
  
Espere que o identificador de entrada atribuído à nova mensagem seja exclusivo, não apenas no repositório de mensagens atual, mas provavelmente em todos os repositórios de mensagens que estejam abertos ao mesmo tempo. Uma exceção a essa regra ocorre quando várias entradas de um repositório de mensagens aparecem no perfil. Isso faz com que o repositório de mensagens seja aberto várias vezes e identificadores de entrada sejam duplicados. 
  
Para criar uma mensagem de saída, chame o método **IMAPIFolder:: CreateMessage** da pasta de saída. 
  
Se você excluir uma pasta que contenha uma nova mensagem antes da mensagem ser salva, os resultados serão indefinidos.
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|FolderDlg. cpp  <br/> |CFolder:: OnNewMessage  <br/> |MFCMAPI usa o método **IMAPIFolder:: CreateMessage** para criar e salvar uma nova mensagem.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

