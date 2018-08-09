---
title: Interfaces do provedor do Outlook Social Connector
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f92b2c7-9f47-4c84-874b-fec1a2a5b555
description: Outlook Social Connector (OSC) é um recurso do Office compartilhado por aplicativos cliente do Office que se conecta ao social e redes de negócios para que os usuários podem permanecer em contato com pessoas em suas redes sem sair do Office.
ms.openlocfilehash: bc393f32e563bbbef70538ea00cd92cf7f96729c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770948"
---
# <a name="outlook-social-connector-provider-interfaces"></a>Interfaces do provedor do Outlook Social Connector

Outlook Social Connector (OSC) é um recurso do Office compartilhado por aplicativos cliente do Office que se conecta ao social e redes de negócios para que os usuários podem permanecer em contato com pessoas em suas redes sem sair do Office. 
  
Um provedor OSC é um modelo COM (Component Object) DLL que permite que o OSC acessar dados de redes sociais de forma independente das APIs de cada rede social. A tabela a seguir lista as interfaces na extensibilidade do provedor OSC. Um provedor OSC deve implementar quatro das interfaces de cinco para se comunicar com o OSC: [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md)e [ISocialSession](isocialsessioniunknown.md). Se o provedor do OSC oferece suporte à sincronização de atividades, sob demanda ou cache de sincronização de híbrido de amigos, cache de credenciais de logon e o logon usando credenciais ou a capacidade de acompanhar uma pessoa, o provedor deve implementar [ISocialSession2 ](isocialsession2iunknown.md), bem como.
  
|**Nome**|**Descrição**|
|:-----|:-----|
|[ISocialPerson](isocialpersoniunknown.md) <br/> |Representa uma pessoa na rede social.  <br/> |
|[ISocialProfile](isocialprofileisocialperson.md) <br/> |Representa o usuário conectado.  <br/> |
|[ISocialProvider](isocialprovideriunknown.md) <br/> |Representa uma instância de um provedor OSC.  <br/> |
|[ISocialSession](isocialsessioniunknown.md) <br/> |Representa uma conexão a um site de rede social.  <br/> |
|[ISocialSession2](isocialsession2iunknown.md) <br/> |Suporte à sincronização de atividades, adicionando amigos, sincronização sob demanda ou híbrida de amigos ou fazer logon na rede social usando credenciais armazenadas em cache.  <br/> |
   

