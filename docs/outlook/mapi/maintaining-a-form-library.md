---
title: Mantendo uma biblioteca de formulários
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
# <a name="maintaining-a-form-library"></a>Mantendo uma biblioteca de formulários

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma biblioteca de formulários contém todas as informações importantes sobre um formulário: suas propriedades, seus verbos e os arquivos executáveis do servidor. Alguns clientes permitem que seus usuários mantenham, instalem ou removam servidores de formulários. Se quiser oferecer esse recurso aos seus usuários, você deve ter acesso ao:
  
- O arquivo de configuração do servidor de formulário, um arquivo com o. Extensão CFG.
    
- O objeto contêiner da biblioteca de formulários, um objeto que implementa a interface [IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md) . 
    
Para acessar o arquivo de configuração ou um nome de caminho para ele, use o que for conveniente. Normalmente, os clientes apresentam ao usuário uma caixa de diálogo para instalar e remover servidores de formulários que também podem ser usados para solicitar ao usuário o local do arquivo de configuração.
  
Para acessar o contêiner da biblioteca de formulários, chame o método [IMAPIFormMgr:: OpenFormContainer](imapiformmgr-openformcontainer.md) do gerente de formulários. Passe um valor de enumeração para especificar qual biblioteca de formulários será aberta e, se necessário, um ponteiro para o objeto que o gerente de formulários deve usar para abrir a biblioteca de formulários. Por exemplo, se você estiver abrindo uma [biblioteca de formulários de pasta](folder-form-libraries.md), passe um ponteiro de [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) . 
  
Após **OpenFormContainer** retornar o ponteiro **IMAPIFormContainer** , chame [IMAPIFormContainer:: InstallForm](imapiformcontainer-installform.md) ou [IMAPIFormContainer:: RemoveForm](imapiformcontainer-removeform.md), dependendo da manutenção a ser executada. **InstallForm** adiciona um servidor de formulários à biblioteca; **RemoveForm** exclui um servidor de formulários da biblioteca. 
  

