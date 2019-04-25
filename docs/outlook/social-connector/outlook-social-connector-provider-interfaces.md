---
title: Interfaces do provedor do Outlook Social Connector
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f92b2c7-9f47-4c84-874b-fec1a2a5b555
description: 'O Outlook Social Connector (OCS) é um recurso do Office compartilhado pelos aplicativos cliente do Office que se conecta a redes empresariais e sociais para que usuários possam se manter em contato com as pessoas das suas redes sem sair do Office. '
ms.openlocfilehash: 77759db34f63239473e0682cfaca720860e96768
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359847"
---
# <a name="outlook-social-connector-provider-interfaces"></a>Interfaces do provedor do Outlook Social Connector

O Outlook Social Connector (OCS) é um recurso do Office compartilhado pelos aplicativos cliente do Office que se conecta a redes empresariais e sociais para que usuários possam se manter em contato com as pessoas das suas redes sem sair do Office.  
  
Um provedor de OSC é um Component Object Model (COM) DLL que permite o OSC acessar dados de redes sociais de forma independente das APIs de cada rede social. A tabela a seguir lista as interfaces na extensibilidade do provedor de OSC. Um provedor de OSC deve implementar quatro das cinco interfaces para se comunicar com o OSC: [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md) e [ISocialSession](isocialsessioniunknown.md). Se o provedor de OSC oferecer suporte a atividades de sincronização, sob demanda ou sincronização híbrida de amigos, armazenar credenciais de logon em cache e fazer logon usando credenciais em cache, ou a capacidade de seguir uma pessoa, o provedor deve também implementar [ISocialSession2](isocialsession2iunknown.md).
  
|**Nome**|**Descrição**|
|:-----|:-----|
|[ISocialPerson](isocialpersoniunknown.md) <br/> |Representa uma pessoa nas redes sociais.  <br/> |
|[ISocialProfile](isocialprofileisocialperson.md) <br/> |Representa o usuário conectado.  <br/> |
|[ISocialProvider](isocialprovideriunknown.md) <br/> |Representa uma instância de um provedor de OSC.  <br/> |
|[ISocialSession](isocialsessioniunknown.md) <br/> |Representa uma conexão a um site de rede social.  <br/> |
|[ISocialSession2](isocialsession2iunknown.md) <br/> |Oferece suporte a atividades de sincronização, adicionar amigos, sob demanda ou sincronização híbrida de amigos, ou fazer logon nas redes sociais usando credenciais em cache.  <br/> |
   

