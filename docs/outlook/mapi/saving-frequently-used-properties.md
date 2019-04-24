---
title: Salvar propriedades usadas com frequência
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a8d4d575-7aa0-4542-91e2-322a6e400551
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: e32ed3388e95d32a4857a933fb735d170dd71688
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283104"
---
# <a name="saving-frequently-used-properties"></a>Salvar propriedades usadas com frequência

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Melhorar o desempenho armazenando dados que levam tempo e recursos a serem recuperados e acessados com frequência. O uso de memória extra pode ser uma opção melhor que recuperações repetidas. Tome cuidado ao criar um cache para armazenar esses dados. Tenha em mente que um cache mal projetado pode impactar negativamente o desempenho.
  
Por exemplo, a maioria dos clientes de mensagem interpessoa (IPM) precisa exibir e abrir a sub-árvore de pastas IPM de várias vezes durante uma sessão típica. Você pode melhorar o desempenho armazenando os identificadores de entrada de cada uma dessas pastas. 
  

