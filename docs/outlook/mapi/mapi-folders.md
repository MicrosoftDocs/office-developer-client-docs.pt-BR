---
title: Pastas MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8fac3c92-d2f5-479e-a368-ca82bddd8e30
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6c00dce9ec489ca2b886f3e51551ba57e9eeea33
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421841"
---
# <a name="mapi-folders"></a>Pastas MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
As pastas são objetos MAPI que servem como a unidade básica da organização para mensagens. Organizar hierarquicamente, as pastas podem conter mensagens e outras pastas. As pastas facilitam a localização e o trabalho com mensagens.
  
As pastas implementam a interface [IMAPIFolder](imapifolderimapicontainer.md) , que herda indiretamente da interface **IUnknown** por meio das interfaces [IMAPIContainer](imapicontainerimapiprop.md) e [IMAPIProp](imapipropiunknown.md) . Os clientes usam o **IMAPIFolder** para criar, copiar e excluir mensagens e pastas, para recuperar e definir o status da mensagem e para definir ou limpar o sinalizador de leitura de uma mensagem. Embora os provedores de repositório de mensagens sejam necessários para dar suporte a todos os métodos no **IMAPIFolder**, alguns métodos introduzem um nível de complexidade que os provedores de repositórios de mensagens podem querer evitar. O MAPI salva provedores de repositórios de mensagens, implementando algumas das funcionalidades de pastas mais complexas na interface [IMAPISupport](imapisupportiunknown.md) . Em vez de implementar seus próprios métodos de cópia, por exemplo, os provedores de repositórios de mensagens podem chamar os métodos Copy no objeto support e obter os mesmos resultados. 
  
Há três tipos de pastas:
  
- Pastas raiz.
    
- Pastas genéricas.
    
- Pastas de pesquisa.
    
Cada repositório de mensagens tem, pelo menos, uma pasta raiz. A pasta raiz aparece na parte superior da hierarquia e contém mensagens e outras pastas. Não é possível mover, copiar, renomear ou excluir pastas raiz. Há apenas uma pasta raiz para cada repositório de mensagens.
  
A maioria das outras pastas são pastas genéricas. Como pastas raiz, as pastas genéricas contêm mensagens e outras pastas. Diferentemente das pastas raiz, elas podem ser movidas, copiadas, renomeadas e excluídas. Pastas genéricas podem ser criadas na pasta raiz ou em outras pastas genéricas. Quando um cliente cria uma pasta genérica em outra pasta, a nova pasta é chamada de subpastas ou pastas filhas. A pasta na qual a nova pasta é colocada é chamada de pasta pai da nova pasta. As pastas genéricas que têm a mesma pasta pai são chamadas de pastas irmãs. Ambas as pastas irmãos e não irmãos podem ou não ter nomes exclusivos, dependendo do provedor de armazenamento de mensagens. Os provedores de repositórios de mensagens que exigem que as pastas irmãs tenham nomes exclusivos retornam o valor de erro MAPI_E_COLLISION quando um cliente tenta criar duas pastas com o mesmo nome no mesmo pai. 
  
Uma pasta de pesquisa contém links para mensagens que correspondem a um conjunto de critérios predefinidos. Como as pastas de pesquisa contêm links em vez de mensagens reais, elas estão em vigor somente leitura. Eles não podem conter outras pastas ou ter mensagens ou pastas movidas ou copiadas para elas. Eles não podem ter novas mensagens criadas neles; e eles próprios não podem ser movidos, copiados ou renomeados. Quando uma mensagem é excluída de uma pasta de pesquisa, ela é realmente excluída da pasta que contém a mensagem.
  
O tipo de pasta é armazenado na propriedade **PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md)). Cada pasta tem essa propriedade definida como FOLDER_GENERIC, FOLDER_ROOT ou FOLDER_SEARCH, dependendo do seu tipo.
  
Cada pasta tem um identificador de entrada e uma chave de registro. O identificador de entrada, **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), é usado por clientes e provedores de serviço para abrir a pasta. A chave de registro, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), é um valor binário usado para comparar a pasta com outras pastas. 
  
Uma pasta tem outras propriedades para identificar pastas relacionadas e o repositório de mensagens. As seguintes propriedades são necessárias:
  
- **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))
    
- **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))
    
- **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))
    
Algumas pastas oferecem suporte à propriedade **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) que descreve o tipo de operação que um usuário pode executar. Por exemplo, uma das configurações válidas para **PR_ACCESS** é MAPI_ACCESS_DELETE, que indica que a pasta pode ser removida. Outra configuração, MAPI_ACCESS_MODIFY, indica que a pasta deve ser modificável. 
  
Para obter uma lista completa das propriedades de pasta obrigatórias, consulte a interface [IMAPIFolder](imapifolderimapicontainer.md) . 
  
## <a name="see-also"></a>Confira também



[Desenvolvimento de aplicativos MAPI](mapi-application-development.md)

