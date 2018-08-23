---
title: Verbos de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a63bf0a7-24e6-4eef-98e8-3744ce5f9f2d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 27999c141fdeb3e1610213db128bc4ad3d049e6d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594095"
---
# <a name="form-verbs"></a>Verbos de formulário

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Normalmente, a interface do usuário de um formulário oferece itens de menu ou controles que permitem que os usuários podem fazer algum tipo de ação com o formulário. É a função do servidor de formulário para lidar com essas ações do usuário. Esta interface é implementada por meio de APIs do Win32 padrão; escrever um é como escrever outras interfaces para programas de Win32 regulares.
  
Muitas vezes, ações do usuário estão associadas a verbos. Um verbo é o nome de uma ação que é específico para uma determinada classe de mensagem. Por exemplo, a **resposta** é um verbo que é implementado por muitos servidores de formulário, cada um deles pode ter uma interpretação diferente da verbo. Verbos às vezes são referidos como comandos. 
  
> [!NOTE]
> Nem todos os itens de menu e controles em um formulário correspondem a um verbo. Por exemplo, um botão **Cancelar** não corresponde a um verbo Cancelar dentro do servidor do formulário. Geralmente, os verbos estão associados a ações que são específicas para uma classe de mensagem específica ou um conjunto de classes de mensagem. Embora as classes de mensagem diferente podem oferecer suporte a diferentes conjuntos de verbos, todos oferecem suporte pelo menos um verbo Open, que exibe a interface do usuário do formulário e o carrega com valores de propriedade da mensagem. 
  
Verbos podem levar sem parâmetros. Formulários que exportam comandos com parâmetros variáveis devem usar os mecanismos de automação.
  
Clientes podem determinar quais verbos são suportados por uma classe de mensagem específica por meio do método [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) , que é implementado pelo gerente de formulário de MAPI. O gerente do formulário obtém essas informações do arquivo de configuração do formulário. O conjunto de acordo com o verbo retornado por esse método é usado pelo cliente para mostrar o usuário os comandos que podem ser executados em uma mensagem. Por exemplo, um cliente pode permitir que os usuários clique com o botão direito do mouse em uma mensagem para exibir os verbos aplicáveis a mensagem. 
  
## <a name="see-also"></a>Confira também

- [Formulários MAPI](mapi-forms.md)

