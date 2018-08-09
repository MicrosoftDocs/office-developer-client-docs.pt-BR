---
title: Registrar um provedor
manager: soliver
ms.date: 03/05/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b60b3634-4c8b-4273-97a0-0a8a5a8a5342
description: Este tópico descreve os locais de registro do Windows que são usados quando você instala um provedor do Outlook Social Connector (OSC).
ms.openlocfilehash: 3ec594ec94b045d2ceb583144781a5746b945b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770944"
---
# <a name="registering-a-provider"></a>Registrar um provedor

Este tópico descreve os locais de registro do Windows que são usados quando você instala um provedor do Outlook Social Connector (OSC).
  
## <a name="com-registration"></a>Registro COM

Você deve configurar o provedor OSC DLL para registrar usando o registro de autoatendimento COM ou regsvr32 durante a instalação. Registro de COM do provedor DLL registra o provedor de OSC sob o `HKEY_CLASSES_ROOT` hive do registro. 
  
Um provedor OSC desenvolvido em código gerenciado tem um assembly do provedor COM visíveis. Você deve usar um domínio de aplicativo separado para o componente do provedor. Caso contrário, o provedor do OSC usa o domínio de aplicativo compartilhado padrão que é usado por outros componentes e o provedor pode não funcionar conforme o esperado.
  
## <a name="registering-provider-progid"></a>Registrando provedor ProgID

Cada provedor OSC deve registrar um identificador de programação (`ProgID`). O instalador do provedor pode escolher um dos seguintes locais para adicionar ou remover o `ProgID`:
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; o instalador do seu provedor deve usar este local, se o provedor está instalado para que apenas o usuário conectado no momento.
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; o instalador do seu provedor deve usar este local, se o provedor está instalado para todos os usuários no computador.
    
O OSC procura o provedor `ProgID` nos locais acima, a menos que o computador cliente tem o Outlook de 32 bits em execução em um sistema de operacional do Windows de 64 bits. Nesse caso, o instalador do seu provedor deve escolher um dos seguintes locais, no `HKEY_CURRENT_USER` ou `HKEY_LOCAL_MACHINE` hive: 
  
- `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
Para obter uma versão Click-to-Run do Office, o instalador do seu provedor deve escolher um dos seguintes locais no hive HKEY_CURRENT_USER ou HKEY_LOCAL_MACHINE:
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Outlook\SocialConnector\SocialProviders`
    
## <a name="see-also"></a>Confira também

- [Lista de verificação de instalação](installation-checklist.md)
- [Etapas rápidas de aprendizado para desenvolver um provedor](quick-steps-for-learning-to-develop-a-provider.md)
- [Implantando um provedor](deploying-a-provider.md)

