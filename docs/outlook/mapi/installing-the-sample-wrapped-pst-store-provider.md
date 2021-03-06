---
title: Instalando o provedor de armazenamento PST com conteúdo de exemplo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 90ce0ea3-ba73-cb57-0fa9-8898bc4ac9de
description: '�ltima altera��o: quinta-feira, 5 de julho de 2012'
ms.openlocfilehash: a1574de555eb74d06c4dbe721e7e013ac59d3071
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309629"
---
# <a name="installing-the-sample-wrapped-pst-store-provider"></a>Instalando o provedor de armazenamento PST com conteúdo de exemplo

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este tópico leva você pelas etapas para baixar e instalar o Provedor de Armazenamento PST com Conteúdo de Amostra. O Sample Wrapped PST Store Provider, WrapPST, implementa um provedor de armazenamento PST empacotado que se destina a ser usado em conjunto com a API de replicação. Para obter mais informações sobre a API de Replicação, consulte [Sobre a API de Replicação.](about-the-replication-api.md)
  
## <a name="install-the-sample-wrapped-pst-store-provider"></a>Instalar o provedor de armazenamento PST com conteúdo de exemplo

1. Para baixar o Exemplo de Provedor de Armazenamento PST, consulte Exemplos de código de referência auxiliar do [Outlook 2007 e Instalador Redistribuível.](https://www.microsoft.com/en-us/download/details.aspx?id=24102)
    
2. Abra a **pasta SampleWrappedPSTStoreProvider** e clique em **Extrair Todos os Arquivos.**
    
3. Clique **em** Procurar, selecione o local onde deseja salvar o exemplo e clique em **OK.**
    
4. Clique em **Extrair**. A pasta selecionada é exibida e contém os arquivos extraídos.
    
5. Abra o Visual Studio 2005 como administrador.
    
    > [!NOTE]
    > Se o computador estiver executando o Windows XP, você deverá estar conectado como administrador. Se o computador estiver executando o Windows Vista, você deverá estar conectado como Administrador e clicar com o botão direito do mouse no ícone do Visual Studio 2005 e clicar em Executar **como administrador.** 
  
6. No Visual Studio 2005, clique em **Arquivo,** selecione **Abrir** e clique em **Projeto/Solução.**
    
7. Navegue até o local onde você salvou o exemplo, clique em **WrapPST** e clique em **Abrir**.
    
8. On the **Build** menu, click **Build Solution**.
    
9. Na caixa **de diálogo Salvar Arquivo como,** clique em **Salvar.**
    
10. Na pasta onde você salvou o exemplo, clique com o botão direito do mouse no **arquivoInstall.bat** e clique em **Executar como administrador.**
    
11. Na caixa de diálogo **Controle de Conta de Usuário**, clique em **Continuar**.
    
## <a name="see-also"></a>Confira também



[Sobre o provedor de armazenamento PST com conteúdo de exemplo](about-the-sample-wrapped-pst-store-provider.md)
  
[Inicializando um provedor de armazenamento PST empacotado](initializing-a-wrapped-pst-store-provider.md)
  
[Fazendo logom em um provedor de armazenamento PST empacotado](logging-on-to-a-wrapped-pst-store-provider.md)
  
[Usando um provedor de armazenamento PST empacotado](using-a-wrapped-pst-store-provider.md)
  
[Desligar um provedor de armazenamento PST empacotado](shutting-down-a-wrapped-pst-store-provider.md)

