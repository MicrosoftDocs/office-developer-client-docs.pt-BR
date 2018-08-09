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
ms.openlocfilehash: b8b30dcc2fcf0c8e75004e36b6fd9f4f4583e304
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770606"
---
# <a name="tnef-correlation"></a>Correlação de TNEF

 
  
**Aplica-se a**: Outlook 
  
Alguns sistemas de mensagens realizar uma verificação de correlação em qualquer fluxo Transport-Neutral Encapsulation Format (TNEF) anexado a uma mensagem de entrada para verificar que o fluxo TNEF na verdade pertencer a mensagem. Isso envolve a correspondência com o valor de algum campo no cabeçalho da mensagem de entrada com uma cópia do valor armazenado na algumas propriedade no stream TNEF. Valores que são provavelmente exclusivos para cada mensagem, como números de identificação de mensagem, geralmente são usados para isso. O transporte ou um gateway que criou o fluxo TNEF é responsável por escolhendo um valor apropriado no cabeçalho da mensagem e fazer uma cópia em uma propriedade adequada antes de codificação de propriedades da mensagem de saída no fluxo TNEF. Gateways ou transportes que recebem a mensagem podem extrair dessa propriedade do stream TNEF e verificar que seu valor corresponde ao valor do campo correspondente do cabeçalho na mensagem de entrada.
  
Se os valores não coincidirem, o gateway ou transporte deve descartar o fluxo TNEF e apenas o envelope de mensagem nativo do processo. Essas verificações são recomendável porque os clientes de email não baseado em MAPI podem anexar um arquivo que contém um fluxo TNEF de uma mensagem antiga para um encaminhamento ou até mesmo uma mensagem não relacionada; Se não estiver marcado, tal erro pode causar perda de texto da mensagem.
  
O valor do campo de cabeçalho escolhido deve ser exclusivo à mensagem. Há nenhum campo de cabeçalho fixa para todos os sistemas de mensagens, como sistemas de mensagens diferentes utilizam campos de cabeçalho diferente, mas normalmente, o sistema de mensagens atribui um identificador exclusivo para a mensagem que é adequada para essa finalidade. Por exemplo, sistemas de SMTP usam geralmente cabeçalho MessageID, enquanto os sistemas de x. 400 geralmente usam o atributo IM_THIS_IPM.
  

