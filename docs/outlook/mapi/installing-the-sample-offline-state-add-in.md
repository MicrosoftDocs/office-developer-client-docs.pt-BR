---
title: Instalar o exemplo de suplemento de estado offline
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: 'Modificado pela última vez: 06 de julho de 2012'
ms.openlocfilehash: 7616c3a6077b9354cda7046c0949e7c5553f6551
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586834"
---
# <a name="installing-the-sample-offline-state-add-in"></a>Instalar o exemplo de suplemento de estado offline

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este tópico leva as etapas para baixar e instalar o suplemento de amostra Offline estado. O suplemento de amostra Offline estado é um suplemento de COM que adiciona um menu de **Estado Offline** para o Outlook e utiliza a API de estado Offline. Através do menu estado Offline, você pode habilitar ou desabilitar o monitoramento do estado, verifique o estado atual e alterar o estado atual. Para obter mais informações sobre como o suplemento de estado Offline é implementado, consulte [Add-in de configuração para cima uma Offline estado](setting-up-an-offline-state-add-in.md).
  
## <a name="install-the-sample-offline-state-add-in"></a>Instalar o amostra Offline State suplemento

1. Baixar o Add-in amostra Offline estado aqui: [amostras de código de referência de auxiliar do Outlook 2007 e instalador redistribuível](http://www.microsoft.com/en-us/download/details.aspx?id=24102).
    
2. Execute o Visual Studio 2005 como administrador.
    
    > [!NOTE]
    > Se seu computador estiver executando o Windows XP, você deve ser logado como administrador. Se seu computador estiver executando o Windows Vista, você deve ser logado como administrador. Com o botão direito no ícone do Visual Studio 2005 e clique em **Executar como administrador**. 
  
3. No Visual Studio 2005, clique em **arquivo**, selecione **Abrir**e, em seguida, clique em **Project/Solution**.
    
4. Navegue até o local onde você salvou a amostra, clique em **ConnectionStateAddin**e, em seguida, clique em **Abrir**.
    
5. On the **Build** menu, click **Build Solution**.
    
6. Na caixa de diálogo **Salvar arquivo como** , clique em **Salvar**.
    
7. Clique no menu **Iniciar** , clique em **Todos os programas**, clique em **Acessórios**, do mouse em **Prompt de comando**e, em seguida, clique **em Executar como administrador**.
    
    > [!NOTE]
    > Se você estiver executando o Windows XP, você deve ser logado como administrador. 
  
8. Na caixa de diálogo **Controle de conta de usuário** , clique em **continuar**.
    
9. Na janela de **Prompt de comando** , altere os diretórios para a pasta de depuração onde você salvou a amostra. Por exemplo, se você salvou a amostra em sua unidade C:\, digite **cd "C:\ConnectionStateAddin\Debug"** e pressione **ENTER**. 
    
10. Digite **regsvr32 OfflineStateAddin.dll** e pressione **ENTER**. 
    
    > [!NOTE]
    > Para desinstalar o suplemento de amostra Offline estado, digite **regsvr32 -u OfflineStateAddin.dll**
  
11. Na caixa de diálogo **regsvr32** , clique em **Okey**.
    
12. Reinicie o Outlook para ver o menu de **Estado Offline** . 
    
## <a name="see-also"></a>Confira também



[Sobre a API de estado offline](about-the-offline-state-api.md)
  
[Instalar o exemplo de suplemento de estado offline](installing-the-sample-offline-state-add-in.md)
  
[Sobre o exemplo de suplemento de estado offline](about-the-sample-offline-state-add-in.md)
  
[Configurar um suplemento de estado offline](setting-up-an-offline-state-add-in.md)
  
[Monitorar alterações de estado da conexão usando um suplemento de estado offline](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[Desconectar-se de um suplemento de estado offline](disconnecting-an-offline-state-add-in.md)

