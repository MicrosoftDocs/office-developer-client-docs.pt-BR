---
title: Pastas MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8fac3c92-d2f5-479e-a368-ca82bddd8e30
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 21b738424b27d3d89d8de84c8c9ff2ff86dd945b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564084"
---
# <a name="mapi-folders"></a>Pastas MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
As pastas são objetos MAPI que servem como a unidade básica de organização para mensagens. Pastas organizados hierarquicamente, podem conter outras pastas e mensagens. Pastas facilitam a localização e trabalhar com mensagens.
  
Pastas implementam a interface de [IMAPIFolder](imapifolderimapicontainer.md) , que herde a interface **IUnknown** através do [IMAPIContainer](imapicontainerimapiprop.md) e interfaces [IMAPIProp](imapipropiunknown.md) indiretamente. Os clientes usam **IMAPIFolder** para criar, copiar e excluir mensagens e pastas, para recuperar e definir o status da mensagem e para definir ou limpar o sinalizador de leitura para uma mensagem. Embora os provedores de armazenamento de mensagem são necessários para dar suporte a todos os métodos **IMAPIFolder**, alguns métodos introduzem um nível de complexidade que os provedores de armazenamento de mensagem talvez queira evitar. MAPI salva os provedores de armazenamento de mensagem algum trabalho por meio da implementação algumas das funcionalidades pasta mais complexas na interface do [IMAPISupport](imapisupportiunknown.md) . Em vez de implementar os métodos de sua própria cópia, por exemplo, provedores de armazenamento de mensagem podem chamar os métodos de cópia do objeto de suporte e obtenha os mesmos resultados. 
  
Existem três tipos de pastas:
  
- Pastas raiz.
    
- Pastas genéricas.
    
- Pastas de pesquisa.
    
Cada armazenamento de mensagens tem pelo menos uma pasta raiz. A pasta raiz aparece na parte superior da hierarquia e contém mensagens e outras pastas. Pastas raiz não podem ser movidas, copiadas, renomeadas ou excluídas. Há apenas uma pasta raiz para cada repositório da mensagem.
  
A maioria das outras pastas são pastas genéricas. Como as pastas raiz, pastas genéricas contêm mensagens e outras pastas. Diferentemente pastas raiz, eles podem ser movidos, copiados, renomeados e excluídos. Pastas genéricas podem ser criadas na pasta raiz ou outras pastas genéricas. Quando um cliente cria uma pasta genérica em outra pasta, a nova pasta é chamada uma subpasta ou pasta filha. A pasta na qual a nova pasta é colocada é conhecida como a pasta pai da nova pasta. Pastas genéricas que possuem a mesma pasta pai são chamadas de pastas irmão. Irmão e não-irmão pastas talvez ou podem não ter nomes exclusivos, dependendo da mensagem o provedor de armazenamento. Provedores de armazenamento de mensagem que exigem pastas irmão ter nomes exclusivos retornar o valor de erro MAPI_E_COLLISION quando um cliente tenta criar duas pastas com o mesmo nome no mesmo pai. 
  
Uma pasta de pesquisa contém links para mensagens que correspondam a um conjunto de critérios predefinidos. Como as pastas de pesquisa contêm links em vez de mensagens reais, eles estarão em vigor somente leitura. Não podem conter outras pastas ou ter mensagens ou pastas movido ou copiadas neles. Eles não podem ter novas mensagens criadas neles; e eles próprios não podem ser movidos, copiados ou renomeados. Quando uma mensagem é excluída de uma pasta de pesquisa, ser realmente excluído da pasta que contém a mensagem.
  
Tipo de pasta é armazenado na propriedade **PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md)). Cada pasta tem esta propriedade definida como FOLDER_GENERIC, FOLDER_ROOT ou FOLDER_SEARCH, dependendo de seu tipo.
  
Cada pasta tem o identificador de uma entrada e uma chave de registro. O identificador de entrada, **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), é usado por clientes e provedores de serviços para abrir a pasta. A chave do registro, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), é um valor binário que é usado para comparar a pasta com outras pastas. 
  
Uma pasta tem outras propriedades para identificar pastas relacionadas e o armazenamento de mensagens. As propriedades a seguir são necessárias:
  
- **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))
    
- **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))
    
- **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))
    
Algumas pastas suportam à propriedade **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) que descreve o tipo de operações que um usuário pode executar. Por exemplo, uma das configurações válidas para **PR_ACCESS** é MAPI_ACCESS_DELETE, que indica que a pasta pode ser removida. Outra configuração, MAPI_ACCESS_MODIFY, indica que a pasta deve ser pode ser modificada. 
  
Para obter uma lista completa das propriedades de pasta necessária, consulte a interface [IMAPIFolder](imapifolderimapicontainer.md) . 
  
## <a name="see-also"></a>Confira também



[Desenvolvimento de aplicativos MAPI](mapi-application-development.md)

