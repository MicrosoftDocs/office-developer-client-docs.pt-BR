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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412629"
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
  
> [in] Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar a nova mensagem. Os identificadores de interface válidos incluem IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer e IID_IMAPIFolder. Passar NULL faz com que o provedor de armazenamento de mensagens retorne a interface de mensagem padrão, [IMessage : IMAPIProp](imessageimapiprop.md). 
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como a mensagem é criada. Os sinalizadores a seguir podem ser definidos:
    
ITEMPROC_FORCE
  
> Indica ao PST (armazenamento de pastas pessoais) que a mensagem está qualificada para processamento de regras antes que o armazenamento notifique qualquer cliente ouvinte sobre a chegada da nova mensagem. O processamento de regras só se aplica a novas mensagens criadas em um servidor que não seja um Microsoft Exchange Server, porque o Exchange Server processa regras para mensagens no servidor. Portanto, o provedor ou cliente que cria a mensagem deve passar esse sinalizador em combinação com o salvar uma mensagem com [IMAPIPProp::SaveChanges](imapiprop-savechanges.md) usando NON_EMS_XP_SAVE, que indica que o servidor não é um Exchange Server. 
    
MAPI_ASSOCIATED 
  
> A mensagem a ser criada deve ser incluída na tabela de conteúdo associada em vez da tabela de conteúdo padrão. As mensagens associadas ficam ocultas da interação do usuário.
    
MAPI_DEFERRED_ERRORS 
  
> **CreateMessage** tem permissão para ser bem-sucedido, mesmo se a operação de criação não tiver sido concluída completamente. Isso significa que a nova mensagem pode não estar disponível imediatamente para o chamador. 
    
 _lppMessage_
  
> [out] Um ponteiro para um ponteiro para a mensagem recém-criada.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A mensagem foi criada com êxito.
    
## <a name="remarks"></a>Comentários

O **método IMAPIFolder::CreateMessage** cria uma nova mensagem com conteúdo genérico ou associado e atribui um identificador de entrada. O identificador de entrada consiste em uma parte que representa o provedor de armazenamento de mensagens e uma parte que representa a mensagem individual. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Você pode optar por definir todas as propriedades de mensagem necessárias em **CreateMessage** ou no método [IMAPIProp::SaveChanges da](imapiprop-savechanges.md) mensagem. Você não precisa disponibilizar essas propriedades até que um salvar com êxito tenha ocorrido. 
  
Para obter mais informações sobre como trabalhar com informações associadas, consulte [Tabelas de](folder-associated-information-tables.md) informações associadas a pastas e tabelas [de conteúdo.](contents-tables.md) 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Alguns provedores de armazenamento de mensagens permitem que o identificador de entrada da nova mensagem seja disponibilizado imediatamente depois que **CreateMessage** retorna; outros provedores de armazenamento de mensagens atrasam sua disponibilidade até que a mensagem seja salva. Como nem todos os provedores de armazenamento de mensagens geram um identificador de entrada para uma nova mensagem até que você tenha chamado o método **IMAPIProp::SaveChanges** da mensagem, talvez não seja possível acessar o identificador de entrada quando **CreateMessage** retornar. Além disso, a nova mensagem pode não ser incluída na tabela de conteúdo da pasta até que ocorra o salvar. 
  
Espere que o identificador de entrada atribuído à nova mensagem seja exclusivo não apenas no armazenamento de mensagens atual, mas provavelmente em todos os armazenamentos de mensagens abertos ao mesmo tempo. Uma exceção a essa regra ocorre quando várias entradas para um armazenamento de mensagens aparecem no perfil. Isso faz com que o armazenamento de mensagens seja aberto várias vezes e identificadores de entrada sejam duplicados. 
  
Para criar uma mensagem de saída, chame o método **IMAPIFolder::CreateMessage** da pasta De saída. 
  
Se você excluir uma pasta que contenha uma nova mensagem antes de a mensagem ser salva, os resultados serão indefinido.
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolder::OnNewMessage  <br/> |MFCMAPI usa o **método IMAPIFolder::CreateMessage** para criar e salvar uma nova mensagem.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

