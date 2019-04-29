---
title: Validando e inicializando um repositório de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 74f0a1fe-2a79-4b32-ab88-85a8839a2639
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 77b3f707fc36a868de5acd7c7ba4642a1da4e3c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433686"
---
# <a name="validating-and-initializing-a-message-store"></a>Validando e inicializando um repositório de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando você abre um repositório de mensagens por meio do método [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) sem definir o sinalizador MDB_NO_MAIL, o MAPI cria várias pastas e atribui nomes e funções padrão. O MAPI é responsável por criar essas pastas para evitar incompatibilidades que, inevitavelmente, ocorreria se os clientes ou provedores de repositórios de mensagens fossem responsáveis pela criação. 
  
Às vezes, é necessário verificar se as pastas apropriadas foram criadas e se elas são válidas. A função [HrValidateIPMSubtree](hrvalidateipmsubtree.md) está disponível para essa finalidade. Se você estiver validando o repositório de mensagens padrão, passe o sinalizador MAPI_FULL_IPM_TREE. Um grupo de pastas mais abrangente é criado para o repositório de mensagens padrão. Quando o **HrValidateIPMSubtree** recebe o sinalizador MAPI_FULL_IPM_TREE, ele verifica as seguintes pastas: 
  
- Pasta raiz da sub-árvore IPM
    
- Pasta itens excluídos na pasta raiz IPM
    
- Pasta caixa de entrada na pasta raiz IPM
    
- Pasta de saída na pasta raiz IPM
    
- Pasta Itens enviados na pasta raiz IPM
    
- Modos de exibição de pasta na pasta raiz do repositório de mensagens
    
- Modos de exibição comuns na pasta raiz do repositório de mensagens
    
- Pasta de pesquisa na pasta raiz do repositório de mensagens
    
Se o repositório de mensagens não for o padrão, você poderá definir ou não o sinalizador MAPI_FULL_IPM_TREE. Quando esse sinalizador não é definido, o **HrValidateIPMSubtree** verifica apenas a pasta raiz da subárvore, a pasta itens excluídos e a pasta raiz dos resultados da pesquisa do repositório de mensagens. 
  
Para inicializar um repositório de mensagens, armazene as seguintes propriedades na memória para que estejam prontamente disponíveis:
  
- **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))
    
- **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))
    
Essas propriedades são bitmasks que descrevem os recursos do repositório de mensagens. O **PR_VALID_FOLDER_MASK** tem um conjunto de bits para cada pasta especial que existe no repositório de mensagens e tem um identificador de entrada atribuído válido. Para obter mais informações sobre como acessar essas pastas e seus identificadores de entrada, consulte [abrir uma pasta de armazenamento de mensagens](opening-a-message-store-folder.md). 
  
 O **PR_STORE_SUPPORT_MASK** tem um conjunto de bits para cada recurso suportado no repositório de mensagens. Por exemplo, se um repositório de mensagens suportar a notificação e o texto formatado, seus **PR_STORE_SUPPORT_MASK** terão os bits STORE_NOTIFY_OK e STORE_RTF_OK definidos. 
  
Outras propriedades que devem ser armazenadas localmente incluem os identificadores de entrada para as pastas que a propriedade **PR_VALID_FOLDER_MASK** descreve como válida. Cada uma dessas pastas especiais, exceto a pasta caixa de entrada, tem uma propriedade de identificador de entrada associada a ela. Por exemplo, o identificador de entrada da pasta de saída é sua propriedade **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)). Como essas pastas são as pastas que serão abertas com frequência, é uma boa ideia ter seus identificadores de entrada prontamente disponíveis.
  

