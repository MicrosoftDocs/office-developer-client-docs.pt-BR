---
title: Instalando o Exemplo de Add-in de Estado Offline
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: 'Last modified: July 06, 2012'
ms.openlocfilehash: b7b9ce539537e0759020ef7e3b4f6541a940d6fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317210"
---
# <a name="installing-the-sample-offline-state-add-in"></a>Instalando o Exemplo de Add-in de Estado Offline

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este tópico leva você pelas etapas para baixar e instalar o Exemplo de Complemento de Estado Offline. O Exemplo de Complemento de Estado Offline é um complemento COM que adiciona um menu Estado **Offline** ao Outlook e utiliza a API de Estado Offline. Por meio do menu Estado Offline, você pode habilitar ou desabilitar o monitoramento de estado, verificar o estado atual e alterar o estado atual. Para obter mais informações sobre como o Complemento de Estado Offline é implementado, consulte Configurando um [complemento de estado offline.](setting-up-an-offline-state-add-in.md)
  
## <a name="install-the-sample-offline-state-add-in"></a>Instalar o Exemplo de Add-in de Estado Offline

1. Baixe o Exemplo de Complemento de Estado Offline aqui: Exemplos de código de referência auxiliar do [Outlook 2007 e instalador redistribuível.](https://www.microsoft.com/en-us/download/details.aspx?id=24102)
    
2. Execute o Visual Studio 2005 como administrador.
    
    > [!NOTE]
    > Se o computador estiver executando o Windows XP, você deverá estar conectado como administrador. Se o computador estiver executando o Windows Vista, você deverá estar conectado como administrador. Clique com o botão direito do mouse no ícone do Visual Studio 2005 e clique **em Executar como administrador.** 
  
3. No Visual Studio 2005, clique em **Arquivo,** selecione **Abrir** e clique em **Projeto/Solução.**
    
4. Navegue até o local onde você salvou o exemplo, clique em **ConnectionStateAddin** e clique em **Abrir**.
    
5. On the **Build** menu, click **Build Solution**.
    
6. Na caixa **de diálogo Salvar Arquivo como,** clique em **Salvar.**
    
7. Clique no menu **Iniciar,** em Todos os **Programas,** **em** Acessórios, clique com o botão direito do mouse em **Prompt** de Comando e clique em Executar **como administrador.**
    
    > [!NOTE]
    > Se você estiver executando o Windows XP, deverá estar conectado como administrador. 
  
8. Na caixa de diálogo **Controle de Conta de Usuário**, clique em **Continuar**.
    
9. Na janela **Prompt de Comando,** altere os diretórios para a pasta Depurar onde você salvou o exemplo. Por exemplo, se você salvou o exemplo em C:\ drive, você digitaria **cd "C:\ConnectionStateAddin\Debug"** e pressione **ENTER**. 
    
10. Digite **regsvr32 OfflineStateAddin.dll** pressione **ENTER**. 
    
    > [!NOTE]
    > Para desinstalar o Exemplo de Complemento de Estado Offline, digite **regsvr32 -u OfflineStateAddin.dll**
  
11. Na caixa **de diálogo RegSrv32,** clique em **OK.**
    
12. Reinicie o Outlook para ver o menu **Estado** Offline. 
    
## <a name="see-also"></a>Confira também



[Sobre a API de estado offline](about-the-offline-state-api.md)
  
[Instalar a amostra de suplemento de estado offline](installing-the-sample-offline-state-add-in.md)
  
[Sobre a amostra de suplemento de estado offline](about-the-sample-offline-state-add-in.md)
  
[Configurar um suplemento de estado offline](setting-up-an-offline-state-add-in.md)
  
[Monitorar alterações de estado da conexão usando um suplemento de estado offline](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[Desconectando um add-in de estado offline](disconnecting-an-offline-state-add-in.md)

