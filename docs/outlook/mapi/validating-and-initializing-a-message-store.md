---
title: Validando e inicializando um armazenamento de mensagens
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
# <a name="validating-and-initializing-a-message-store"></a>Validando e inicializando um armazenamento de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando você abre um repositório de mensagens por meio do método [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) sem definir o sinalizador MDB_NO_MAIL, o MAPI cria várias pastas e atribui a elas nomes e funções padrão. A MAPI é responsável por criar essas pastas para evitar as incompatibilidades que inevitavelmente ocorreriam se clientes ou provedores de armazenamento de mensagens fossem responsáveis pela criação. 
  
Às vezes, é necessário verificar se as pastas apropriadas foram criadas e se são válidas. A [função HrValidateIPMSubtree](hrvalidateipmsubtree.md) está disponível para essa finalidade. Se você estiver validando o armazenamento de mensagens padrão, passe o sinalizador MAPI_FULL_IPM_TREE mensagem. Um grupo mais extenso de pastas é criado para o armazenamento de mensagens padrão. Quando **HrValidateIPMSubtree** recebe o sinalizador MAPI_FULL_IPM_TREE, ele verifica as seguintes pastas: 
  
- Pasta raiz da subárvore do IPM
    
- Pasta Itens Excluídos na pasta raiz do IPM
    
- Pasta caixa de entrada na pasta raiz do IPM
    
- Pasta caixa de saída na pasta raiz do IPM
    
- Pasta Itens Enviados na pasta raiz do IPM
    
- Exibições de pasta na pasta raiz do armazenamento de mensagens
    
- Exibições comuns na pasta raiz do armazenamento de mensagens
    
- Pasta de pesquisa na pasta raiz do armazenamento de mensagens
    
Se o armazenamento de mensagens não for o padrão, você poderá definir ou não o sinalizador MAPI_FULL_IPM_TREE mensagem. Quando esse sinalizador não está definido, **HrValidateIPMSubtree** verifica somente a pasta raiz da subárvore, a pasta Itens Excluídos e a pasta raiz dos resultados de pesquisa do armazenamento de mensagens. 
  
Para inicializar um armazenamento de mensagens, armazene as seguintes propriedades na memória para que elas sejam prontamente disponíveis:
  
- **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))
    
- **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))
    
Essas propriedades são bitmasks que descrevem os recursos do armazenamento de mensagens. **PR_VALID_FOLDER_MASK** tem um bit definido para cada pasta especial que existe no armazenamento de mensagens e tem um identificador de entrada atribuído que é válido. Para obter mais informações sobre como acessar essas pastas e seus identificadores de entrada, consulte [Abrindo uma pasta do armazenamento de mensagens.](opening-a-message-store-folder.md) 
  
 **PR_STORE_SUPPORT_MASK** tem um bit definido para cada recurso com suporte no armazenamento de mensagens. Por exemplo, se um armazenamento de mensagens  suportar a notificação e o texto formatado, sua PR_STORE_SUPPORT_MASK terá os bits STORE_NOTIFY_OK e STORE_RTF_OK bits definidos. 
  
Outras propriedades que devem ser armazenadas localmente incluem os identificadores de entrada para as pastas que a PR_VALID_FOLDER_MASK **propriedade** descreve como válida. Cada uma dessas pastas especiais, exceto a pasta Caixa de Entrada, tem uma propriedade de identificador de entrada associada a ela. Por exemplo, o identificador de entrada para a pasta Caixa de Saída é sua **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) . Como essas pastas são as que serão abertas com frequência, é uma boa ideia ter seus identificadores de entrada prontamente disponíveis.
  

