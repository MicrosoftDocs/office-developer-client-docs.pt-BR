---
title: Instalar o exemplo de suplemento de estado offline
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: 'Última modificação: 06 de julho de 2012'
ms.openlocfilehash: b7b9ce539537e0759020ef7e3b4f6541a940d6fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317210"
---
# <a name="installing-the-sample-offline-state-add-in"></a>Instalar o exemplo de suplemento de estado offline

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este tópico orienta as etapas para baixar e instalar o exemplo de suplemento de estado offline. O exemplo de suplemento de estado offline é um suplemento de COM que adiciona um menu de **estado offline** ao Outlook e utiliza a API de estado offline. No menu de estado offline, você pode habilitar ou desabilitar o monitoramento de estado, verificar o estado atual e alterar o estado atual. Para obter mais informações sobre como o suplemento de estado offline é implementado, consulte [Configurando um suplemento de estado offline](setting-up-an-offline-state-add-in.md).
  
## <a name="install-the-sample-offline-state-add-in"></a>Instalar o exemplo de suplemento de estado offline

1. Baixe o exemplo de suplemento offline State aqui: [exemplos de código de referência auxiliar do Outlook 2007 e instalador](https://www.microsoft.com/en-us/download/details.aspx?id=24102)redistribuível.
    
2. Execute o Visual Studio 2005 como um administrador.
    
    > [!NOTE]
    > Se o computador estiver executando o Windows XP, você deverá estar conectado como administrador. Se o computador estiver executando o Windows Vista, você deverá estar conectado como administrador. Clique com o botão direito do mouse no ícone do Visual Studio 2005 e clique em **Executar como administrador**. 
  
3. No Visual Studio 2005, clique em **arquivo**, selecione **abrir**e, em seguida, clique em **projeto/solução**.
    
4. Navegue até o local onde você salvou o exemplo, clique em **ConnectionStateAddin**e, em seguida, clique em **abrir**.
    
5. On the **Build** menu, click **Build Solution**.
    
6. Na caixa de diálogo **salvar arquivo como** , clique em **salvar**.
    
7. Clique no menu **Iniciar** , em **todos os programas**, em **acessórios**, clique com o botão direito do mouse em prompt de **comando**e clique em **Executar como administrador**.
    
    > [!NOTE]
    > Se você estiver executando o Windows XP, você deve estar conectado como um administrador. 
  
8. Na caixa de diálogo **Controle de Conta de Usuário**, clique em **Continuar**.
    
9. Na janela de **prompt de comando** , altere os diretórios para a pasta de depuração onde você salvou o exemplo. Por exemplo, se você salvou o exemplo em C:\ Digite **CD "C:\ConnectionStateAddin\Debug"** e pressione **Enter**. 
    
10. Digite **regsvr32 OfflineStateAddin. dll** e pressione **Enter**. 
    
    > [!NOTE]
    > Para desinstalar o exemplo de suplemento de estado offline, digite **regsvr32-u OfflineStateAddin. dll**
  
11. Na caixa de diálogo **RegSrv32** , clique em **OK**.
    
12. ReInicie o Outlook para ver o menu de **estado offline** . 
    
## <a name="see-also"></a>Confira também



[Sobre a API de estado offline](about-the-offline-state-api.md)
  
[Instalar a amostra de suplemento de estado offline](installing-the-sample-offline-state-add-in.md)
  
[Sobre a amostra de suplemento de estado offline](about-the-sample-offline-state-add-in.md)
  
[Configurar um suplemento de estado offline](setting-up-an-offline-state-add-in.md)
  
[Monitorar alterações de estado da conexão usando um suplemento de estado offline](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[Desconectar um suplemento de estado offline](disconnecting-an-offline-state-add-in.md)

