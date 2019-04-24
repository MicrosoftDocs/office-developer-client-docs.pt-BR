---
title: Correlação de TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 93d1716d-a0be-45aa-85d2-6c9be65f5fd2
description: 'Última modificação: 12 de março de 2013'
ms.openlocfilehash: 8d601bb2bbc65e21c5bc83179cc29e53ddd33876
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327394"
---
# <a name="tnef-correlation"></a>Correlação de TNEF

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Alguns sistemas de mensagens realizam uma verificação de correlação em qualquer fluxo de formato de encapsulamento de transporte neutro (TNEF) anexado a uma mensagem de entrada para verificar se o fluxo TNEF faz parte do fato pertence a essa mensagem. Isso envolve a correspondência do valor de algum campo no cabeçalho da mensagem de entrada com uma cópia do valor armazenado em alguma propriedade no fluxo TNEF. Os valores que são supostamente exclusivos para cada mensagem, como números de ID de mensagem, são normalmente usados para isso. O transporte ou gateway que criou o fluxo TNEF é responsável por escolher um valor apropriado do cabeçalho da mensagem e colocar uma cópia em uma propriedade apropriada antes de codificar as propriedades da mensagem de saída no fluxo TNEF. Gateways ou transportes que recebem a mensagem podem então extrair essa propriedade do fluxo TNEF e verificar se o valor corresponde ao valor do campo de cabeçalho correspondente na mensagem de entrada.
  
Se os valores não corresponderem, o gateway ou transporte deverá descartar o fluxo TNEF e processar apenas o envelope de mensagem nativo. Essas verificações são prudentes porque clientes de email não baseados em MAPI podem anexar um arquivo que contém um fluxo TNEF de uma mensagem antiga para uma mensagem de encaminhamento ou até mesmo uma inrelacionada; Se não for selecionada, tal erro poderá causar a perda de texto da mensagem.
  
O valor do campo de cabeçalho escolhido deve ser exclusivo da mensagem. Não há nenhum campo de cabeçalho fixo para todos os sistemas de mensagens porque diferentes sistemas de mensagens usam diferentes campos de cabeçalho, mas geralmente o sistema de mensagens atribui um identificador exclusivo à mensagem que é adequada para essa finalidade. Por exemplo, os sistemas SMTP normalmente usam o cabeçalho MessageID, enquanto os sistemas X. 400 normalmente usam o atributo IM_THIS_IPM.
  

