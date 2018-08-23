---
title: Instalar o provedor do repositório PST encapsulado de exemplo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 90ce0ea3-ba73-cb57-0fa9-8898bc4ac9de
description: '�ltima altera��o: quinta-feira, 5 de julho de 2012'
ms.openlocfilehash: 5b16da68a5cc5ab9e005a262bf1518ea90aac570
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587534"
---
# <a name="installing-the-sample-wrapped-pst-store-provider"></a>Instalar o provedor do repositório PST encapsulado de exemplo

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este tópico leva as etapas para baixar e instalar o provedor de repositórios de PST quebrado automaticamente amostra. O provedor de repositório PST de quebradas amostra, WrapPST, implementa um provedor de armazenamento com quebra PST que se destina a ser usado em conjunto com a API de replicação. Para obter mais informações sobre a API de replicação, consulte [Sobre o API de replicação](about-the-replication-api.md).
  
## <a name="install-the-sample-wrapped-pst-store-provider"></a>Instale o fornecedor de repositório PST encapsulado da amostra

1. Para baixar o provedor de repositórios de PST quebrado automaticamente amostra, consulte [exemplos de código de referência de auxiliar do Outlook 2007 e instalador redistribuível](http://www.microsoft.com/en-us/download/details.aspx?id=24102).
    
2. Abra a pasta **SampleWrappedPSTStoreProvider** e clique em **Extrair todos os arquivos**.
    
3. Clique em **Procurar**, selecione o local onde deseja salvar a amostra e clique em **Okey**.
    
4. Clique em **extrair**. A pasta selecionada é exibida e contém os arquivos extraídos.
    
5. Abra o Visual Studio 2005 como administrador.
    
    > [!NOTE]
    > Se seu computador estiver executando o Windows XP, você deve ser logado como administrador. Se seu computador estiver executando o Windows Vista, você deve estar logado como administrador e você deve com o botão direito no ícone do Visual Studio 2005 e clique em **Executar como administrador**. 
  
6. No Visual Studio 2005, clique em **arquivo**, selecione **Abrir**e, em seguida, clique em **Project/Solution**.
    
7. Navegue até o local onde você salvou a amostra, clique em **WrapPST**e, em seguida, clique em **Abrir**.
    
8. On the **Build** menu, click **Build Solution**.
    
9. Na caixa de diálogo **Salvar arquivo como** , clique em **Salvar**.
    
10. Na pasta onde você salvou a amostra, com o botão direito do arquivo **Install. bat** e clique em **Executar como administrador**.
    
11. Na caixa de diálogo **Controle de conta de usuário** , clique em **continuar**.
    
## <a name="see-also"></a>Confira também



[Sobre o exemplo de provedor do repositório PST encapsulado](about-the-sample-wrapped-pst-store-provider.md)
  
[Iniciar um provedor do repositório PST encapsulado](initializing-a-wrapped-pst-store-provider.md)
  
[Fazer logon em um provedor do repositório PST encapsulado](logging-on-to-a-wrapped-pst-store-provider.md)
  
[Usar um provedor do repositório PST encapsulado](using-a-wrapped-pst-store-provider.md)
  
[Desativar um provedor do repositório PST encapsulado](shutting-down-a-wrapped-pst-store-provider.md)

