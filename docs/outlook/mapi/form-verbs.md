---
title: Verbos de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a63bf0a7-24e6-4eef-98e8-3744ce5f9f2d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: dbd08437dfdd38c3a43cbf12eae8710cc8e3661e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327486"
---
# <a name="form-verbs"></a>Verbos de formulário

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A interface de usuário de um formulário normalmente oferece itens de menu ou controles que permitem que os usuários executem algum tipo de ação com o formulário. É o trabalho do servidor de formulário para lidar com essas ações do usuário. Essa interface é implementada usando as APIs padrão do Win32; escrever um é como escrever outras interfaces para programas normais do Win32.
  
Frequentemente, as ações do usuário são associadas a verbos. Um verbo é o nome de uma ação específica para uma determinada classe de mensagem. Por exemplo, **Reply** é um verbo que é implementado por muitos servidores de formulário, cada um deles pode ter uma interpretação diferente desse verbo. Às vezes, os verbos são chamados de comandos. 
  
> [!NOTE]
> Nem todos os itens de menu e controles em um formulário correspondem a um verbo. Por exemplo, um botão **Cancelar** não corresponde a um verbo cancelar no servidor de formulários. Normalmente, os verbos são associados a ações específicas de uma determinada classe de mensagem ou de um conjunto de classes de mensagem. Embora diferentes classes de mensagens possam suportar diferentes conjuntos de verbos, todos dão suporte ao mínimo de verbo aberto, que exibe a interface do usuário do formulário e o carrega com os valores de propriedade da mensagem. 
  
Os verbos podem não receber parâmetros. Formulários que exportam comandos com parâmetros variáveis devem usar mecanismos de automação.
  
Os clientes podem determinar quais verbos são compatíveis com uma determinada classe de mensagens por meio do método [IMAPIFormInfo:: CalcVerbSet](imapiforminfo-calcverbset.md) , que é implementado pelo Gerenciador de formulários MAPI. O gerente de formulários obtém essas informações no arquivo de configuração do formulário. O conjunto de verbos retornado por esse método é usado pelo cliente para mostrar o usuário quais comandos podem ser executados em uma mensagem. Por exemplo, um cliente pode permitir que os usuários cliquem com o botão direito do mouse sobre uma mensagem para exibir verbos aplicáveis a essa mensagem. 
  
## <a name="see-also"></a>Confira também

- [Formulários MAPI](mapi-forms.md)

