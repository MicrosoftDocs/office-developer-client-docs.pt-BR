---
title: Excluir um perfil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d01ab2e-40fd-409d-a69d-163b7d5462ca
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1cd87b92a9d289f06e466f4e44ce757c93074336
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316825"
---
# <a name="deleting-a-profile"></a>Excluir um perfil

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 **Para excluir um perfil**
  
- Chamar [IProfAdmin::D eleteprofile](iprofadmin-deleteprofile.md).
    
 **DeleteProfile** marca o perfil para exclusão, se estiver sendo usado no momento, aguardando até que não esteja mais ativo para removê-lo. O perfil não desaparece, de fato, até que todos os clientes com uma sessão ativa tenham sido desconectados. 
  
 **DeleteProfile** chama a função de ponto de entrada de cada serviço de mensagens no perfil com o parâmetro _ULCONTEXT_ definido como MSG_SERVICE_DELETE. As chamadas para as funções de ponto de entrada ocorrem antes de os serviços serem removidos fisicamente do perfil. 
  

