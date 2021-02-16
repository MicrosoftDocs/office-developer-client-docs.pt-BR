---
title: Mantendo uma biblioteca de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8488f7ec-e44b-4d1a-ba42-baea8c71d350
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 51c7c3f8ba70dcb3d35dc50806e984fd4b193818
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408800"
---
# <a name="maintaining-a-form-library"></a>Mantendo uma biblioteca de formulário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma biblioteca de formulário contém todas as informações importantes sobre um formulário: suas propriedades, seus verbos e seus arquivos executáveis do servidor. Alguns clientes permitem que seus usuários mantenham, instalem ou removam servidores de formulário. Se quiser oferecer esse recurso aos usuários, você deve ter acesso a:
  
- O arquivo de configuração do servidor de formulário, um arquivo com o . Extensão CFG.
    
- O objeto contêiner da biblioteca de formulário, um objeto que implementa [o IMAPIFormContainer : interface IUnknown.](imapiformcontaineriunknown.md) 
    
Para acessar o arquivo de configuração ou um nome de caminho a ele, use qualquer meio que seja conveniente. Normalmente, os clientes apresentam ao usuário uma caixa de diálogo para instalar e remover servidores de formulário que também podem ser usados para solicitar ao usuário o local do arquivo de configuração.
  
Para acessar o contêiner da biblioteca de formulário, chame o método [IMAPIFormMgr::OpenFormContainer do](imapiformmgr-openformcontainer.md) gerenciador de formulário. Passe um valor de enumeração para especificar qual biblioteca de formulário abrir e, se necessário, um ponteiro para o objeto que o gerenciador de formulário deve usar para abrir a biblioteca de formulário. For example, if you are opening a [Folder Form Libraries](folder-form-libraries.md), pass an [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) pointer. 
  
Depois que **OpenFormContainer** retornar o ponteiro **IMAPIFormContainer,** chame [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) ou [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md), dependendo da manutenção a ser executada. **InstallForm** adiciona um servidor de formulário à biblioteca; **RemoveForm** exclui um servidor de formulário da biblioteca. 
  

