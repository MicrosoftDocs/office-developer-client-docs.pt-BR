---
title: Manter uma biblioteca de formulários
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8488f7ec-e44b-4d1a-ba42-baea8c71d350
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6713055837e3b9b664d5fa1465c9a889919ee5ed
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590089"
---
# <a name="maintaining-a-form-library"></a>Manter uma biblioteca de formulários

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma biblioteca de formulários contém todas as informações importantes sobre um formulário: arquivos executáveis do seu servidor, seus verbos e suas propriedades. Alguns clientes permitir que seus usuários a manter, instalar ou remover servidores de formulário. Se você deseja oferecer esse recurso para seus usuários, você deve ter acesso ao:
  
- Arquivo de configuração do servidor de formulário, um arquivo com o. Extensão de configuração.
    
- Objeto de contêiner da biblioteca de formulários, um objeto que implementa o [IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md) interface. 
    
Para acessar o arquivo de configuração ou um nome de caminho a ela, use qualquer meio é conveniente. Geralmente, os clientes apresentam ao usuário com uma caixa de diálogo de instalação e remoção de servidores de formulário que também podem ser usados para avisar o usuário para o local do arquivo de configuração.
  
Para acessar o contêiner da biblioteca de formulários, chame o método de [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) do gerente do formulário. Passe um valor de enumeração para especificar qual biblioteca de formulários para abrir e se necessário, um ponteiro para o objeto que o gerente do formulário deve usar para abrir a biblioteca de formulários. Por exemplo, se você está abrindo uma [Pasta bibliotecas de formulários](folder-form-libraries.md), passe uma [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) ponteiro. 
  
Após **OpenFormContainer** retorna o ponteiro **IMAPIFormContainer** , chame Update [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) ou [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md), dependendo de manutenção a ser executada. **InstallForm** adiciona um servidor de formulário para a biblioteca; **RemoveForm** exclui um servidor de formulário da biblioteca. 
  

