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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410368"
---
# <a name="tnef-correlation"></a>Correlação de TNEF

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Alguns sistemas de mensagens executam uma verificação de correlação em qualquer fluxo de formato de encapsulamento do Transport-Neutral (TNEF) anexado a uma mensagem de entrada para verificar se o fluxo TNEF realmente pertence a essa mensagem. Isso envolve a correspondência do valor de algum campo no header da mensagem de entrada com uma cópia desse valor armazenada em alguma propriedade no fluxo TNEF. Valores que são aparentemente exclusivos para cada mensagem, como números de ID de mensagens, são normalmente usados para isso. O transporte ou gateway que criou o fluxo TNEF é responsável por escolher um valor apropriado do header da mensagem e colocar uma cópia em uma propriedade apropriada antes de codificar as propriedades da mensagem de saída para o fluxo TNEF. Gateways ou transportes que recebem a mensagem podem extrair essa propriedade do fluxo TNEF e verificar se seu valor corresponde ao valor do campo de header correspondente na mensagem de entrada.
  
Se os valores não corresponderem, o gateway ou o transporte deverá descartar o fluxo TNEF e processar somente o envelope de mensagem nativa. Essas verificações são prudentes porque clientes de email não baseados em MAPI podem anexar um arquivo que contém um fluxo TNEF de uma mensagem antiga a um encaminhamento ou até mesmo a uma mensagem não relacionada; se não estiver marcado, esse erro poderá causar a perda de texto da mensagem.
  
O valor do campo de header escolhido deve ser exclusivo da mensagem. Não há um campo de título fixo para todos os sistemas de mensagens porque sistemas de mensagens diferentes usam campos de título diferentes, mas normalmente o sistema de mensagens atribui um identificador exclusivo à mensagem que é adequada para essa finalidade. Por exemplo, os sistemas SMTP normalmente usam o header MessageID, enquanto os sistemas X.400 normalmente usam o IM_THIS_IPM atributo.
  

