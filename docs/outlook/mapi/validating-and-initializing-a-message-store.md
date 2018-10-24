---
title: Validar e inicializar um repositório de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 74f0a1fe-2a79-4b32-ab88-85a8839a2639
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7a5a5045594e87953d967fddbdeefd5ac18c8a3d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581969"
---
# <a name="validating-and-initializing-a-message-store"></a>Validar e inicializar um repositório de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando você abre um armazenamento de mensagens por meio do método [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) sem definir o sinalizador MDB_NO_MAIL, MAPI cria várias pastas e os atribui funções e os nomes padrão. MAPI é responsável por criar essas pastas para evitar incompatibilidades que ocorreriam inevitavelmente fossem clientes ou provedores de armazenamento de mensagem responsáveis pela criação. 
  
Em alguns casos, é necessário verificar se as pastas apropriadas foram criadas e que são válidos. A função [HrValidateIPMSubtree](hrvalidateipmsubtree.md) está disponível para essa finalidade. Se você estiver validando o armazenamento de mensagens padrão, passe o sinalizador MAPI_FULL_IPM_TREE. Um grupo mais abrangente de pastas é criado para o armazenamento de mensagens padrão. Quando **HrValidateIPMSubtree** recebe o sinalizador MAPI_FULL_IPM_TREE, ele verifica as seguintes pastas: 
  
- Pasta raiz para a subárvore IPM
    
- Pasta de itens excluídos na pasta raiz IPM
    
- Pasta de caixa de entrada na pasta raiz IPM
    
- Pasta na pasta raiz IPM caixa de saída
    
- Pasta Itens enviados na pasta raiz IPM
    
- Modos de exibição de pasta na pasta raiz do repositório de mensagem
    
- Modos de exibição comuns na pasta raiz do repositório de mensagem
    
- Pasta de pesquisa na pasta raiz do repositório de mensagem
    
Se o armazenamento de mensagens não é o padrão, você pode definir ou não definir o sinalizador MAPI_FULL_IPM_TREE. Quando esse sinalizador não estiver definida, **HrValidateIPMSubtree** procura somente a pasta raiz para a subárvore, a pasta Itens excluídos e a pasta raiz de mensagem armazenam os resultados da pesquisa. 
  
Para inicializar um armazenamento de mensagens, armazene as seguintes propriedades na memória, para que sejam prontamente disponíveis:
  
- **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))
    
- **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))
    
Essas propriedades são máscaras de bits que descrevem os recursos de armazenamento de mensagens. **PR_VALID_FOLDER_MASK** tem um bit definido para cada pasta especial que existe no armazenamento de mensagens e tem um identificador de entrada atribuídas que é válido. Para obter mais informações sobre o acesso a essas pastas e seus identificadores de entrada, consulte [abrindo uma pasta de repositório de mensagem](opening-a-message-store-folder.md). 
  
 **PR_STORE_SUPPORT_MASK** tem um bit definido para cada recurso compatíveis com o armazenamento de mensagens. Por exemplo, se um armazenamento de mensagens oferece suporte a notificação e texto formatado, seu **PR_STORE_SUPPORT_MASK** terá o conjunto de bits STORE_NOTIFY_OK e STORE_RTF_OK. 
  
Outras propriedades que devem ser armazenadas localmente incluem os identificadores de entrada para as pastas que a propriedade **PR_VALID_FOLDER_MASK** descreve como válido. Cada uma dessas pastas especiais, exceto para a pasta de caixa de entrada, tem uma propriedade de identificador de entrada associada a ela. Por exemplo, o identificador de entrada para a pasta caixa de saída é sua propriedade **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)). Como essas pastas são as pastas que serão abertas com frequência, é uma boa ideia ter seus identificadores de entrada prontamente disponíveis.
  

