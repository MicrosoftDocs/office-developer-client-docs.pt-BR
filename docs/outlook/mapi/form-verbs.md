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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424025"
---
# <a name="form-verbs"></a>Verbos de formulário

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A interface do usuário de um formulário normalmente oferece itens de menu ou controles que permitem que os usuários tomem algum tipo de ação com o formulário. É trabalho do servidor de formulário lidar com essas ações do usuário. Essa interface é implementada usando APIs win32 padrão; escrever uma é exatamente como escrever outras interfaces para programas Win32 regulares.
  
Muitas vezes, as ações do usuário são associadas a verbos. Um verbo é o nome de uma ação específica de uma determinada classe de mensagem. Por exemplo, **Responder** é um verbo implementado por muitos servidores de formulário, cada um deles pode ter uma interpretação diferente desse verbo. Verbos são, às vezes, chamados de comandos. 
  
> [!NOTE]
> Nem todos os itens de menu e controles em um formulário correspondem a um verbo. Por exemplo, um **botão Cancelar** não corresponde a um verbo Cancelar no servidor de formulário. Normalmente, os verbos são associados a ações específicas de uma classe de mensagem específica ou a um conjunto de classes de mensagens. Embora classes de mensagens diferentes possam dar suporte a diferentes conjuntos de verbos, todas suportam pelo menos o verbo Open, que exibe a interface do usuário do formulário e a carrega com os valores de propriedade da mensagem. 
  
Verbos podem não ter parâmetros. Formulários que exportam comandos com parâmetros variáveis devem usar os mecanismos de Automação.
  
Os clientes podem determinar quais verbos são suportados por uma classe de mensagem específica por meio do método [IMAPIFormInfo::CalcVerbSet,](imapiforminfo-calcverbset.md) que é implementado pelo gerenciador de formulário MAPI. O gerenciador de formulário obtém essas informações do arquivo de configuração do formulário. O conjunto de verbos retornado por esse método é usado pelo cliente para mostrar ao usuário quais comandos podem ser executados em uma mensagem. Por exemplo, um cliente pode permitir que os usuários cliquem no botão direito do mouse sobre uma mensagem para exibir verbos aplicáveis a essa mensagem. 
  
## <a name="see-also"></a>Confira também

- [Formulários MAPI](mapi-forms.md)

