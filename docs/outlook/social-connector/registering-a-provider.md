---
title: Registrar um provedor
manager: soliver
ms.date: 03/05/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b60b3634-4c8b-4273-97a0-0a8a5a8a5342
description: Este tópico descreve os locais do Registro do Windows que são usados quando você instala um provedor do Outlook Social Connector (OSC).
ms.openlocfilehash: a5f76850f9bebcba3c2bff31e799a3b012d6b91a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421757"
---
# <a name="registering-a-provider"></a>Registrar um provedor

Este tópico descreve os locais do Registro do Windows que são usados quando você instala um provedor do Outlook Social Connector (OSC).
  
## <a name="com-registration"></a>Registro COM

Você deve configurar a DLL do provedor OSC para se registrar usando o auto-registro COM ou regsvr32 durante a instalação. O registro COM da DLL do provedor registra o provedor OSC no `HKEY_CLASSES_ROOT` hive do Registro. 
  
Um provedor OSC desenvolvido em código gerenciado tem um assembly de provedor visível para COM. Você deve usar um domínio de aplicativo separado para o componente do provedor. Caso contrário, o provedor OSC usará o domínio de aplicativo compartilhado padrão usado por outros componentes, e o provedor poderá não operar conforme o esperado.
  
## <a name="registering-provider-progid"></a>Registrar o ProgID do provedor

Cada provedor OSC deve registrar um identificador programático ( `ProgID` ). O instalador do provedor pode escolher um dos seguintes locais para adicionar ou remover `ProgID` o:
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`O instalador do provedor deverá usar esse local se o provedor estiver instalado apenas para o usuário conectado &ndash; no momento.
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash;O instalador do provedor deverá usar esse local se o provedor estiver instalado para todos os usuários no computador.
    
O OSC procura o provedor nos locais acima, a menos que o computador cliente tenha o Outlook de 32 bits em execução em um sistema operacional Windows de  `ProgID` 64 bits. Nesse caso, o instalador do provedor deve escolher um dos seguintes locais no  `HKEY_CURRENT_USER`  `HKEY_LOCAL_MACHINE` hive ou no hive: 
  
- `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
Para uma versão Clique para Executar do Office, o instalador do provedor deve escolher um dos seguintes locais no HKEY_CURRENT_USER ou HKEY_LOCAL_MACHINE hive:
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Outlook\SocialConnector\SocialProviders`
    
## <a name="see-also"></a>Confira também

- [Lista de verificação da instalação](installation-checklist.md)
- [Etapas rápidas para aprender a desenvolver um provedor](quick-steps-for-learning-to-develop-a-provider.md)
- [Implantar um provedor](deploying-a-provider.md)

