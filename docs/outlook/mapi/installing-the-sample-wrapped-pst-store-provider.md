---
title: Instalando o provedor de repositório PST encapsulado de exemplo
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
# <a name="installing-the-sample-wrapped-pst-store-provider"></a>Instalando o provedor de repositório PST encapsulado de exemplo

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este tópico orienta as etapas para baixar e instalar o exemplo de provedor de repositório PST encapsulado. O exemplo de provedor de repositório PST encapsulado, WrapPST, implementa um provedor de repositório PST encapsulado que deve ser usado em conjunto com a API de replicação. Para obter mais informações sobre a API de replicação, consulte [About The Replication API](about-the-replication-api.md).
  
## <a name="install-the-sample-wrapped-pst-store-provider"></a>Instalar o exemplo de provedor de repositório PST encapsulado

1. Para baixar o exemplo de provedor de repositório PST encapsulado, confira [exemplos de código de referência auxiliar do Outlook 2007 e instalador](https://www.microsoft.com/en-us/download/details.aspx?id=24102)redistribuível.
    
2. Abra a pasta **SampleWrappedPSTStoreProvider** e clique em **extrair todos os arquivos**.
    
3. Clique em **procurar**, selecione o local onde deseja salvar o exemplo e clique em **OK**.
    
4. Clique em **Extrair**. A pasta selecionada aparece e contém os arquivos extraídos.
    
5. Abra o Visual Studio 2005 como um administrador.
    
    > [!NOTE]
    > Se o computador estiver executando o Windows XP, você deverá estar conectado como administrador. Se seu computador está executando o Windows Vista, você deve estar conectado como administrador e deve clicar com o botão direito do mouse no ícone do Visual Studio 2005 e clicar em **Executar como administrador**. 
  
6. No Visual Studio 2005, clique em **arquivo**, selecione **abrir**e, em seguida, clique em **projeto/solução**.
    
7. Navegue até o local onde você salvou o exemplo, clique em **WrapPST**e, em seguida, clique em **abrir**.
    
8. On the **Build** menu, click **Build Solution**.
    
9. Na caixa de diálogo **salvar arquivo como** , clique em **salvar**.
    
10. Na pasta onde você salvou o exemplo, clique com o botão direito do mouse no arquivo **install. bat** e clique em **Executar como administrador**.
    
11. Na caixa de diálogo **Controle de Conta de Usuário**, clique em **Continuar**.
    
## <a name="see-also"></a>Confira também



[Sobre o exemplo de provedor de repositório PST encapsulado](about-the-sample-wrapped-pst-store-provider.md)
  
[Inicializando um provedor de repositório PST encapsulado](initializing-a-wrapped-pst-store-provider.md)
  
[Fazer logon em um provedor de repositório PST encapsulado](logging-on-to-a-wrapped-pst-store-provider.md)
  
[Usando um provedor de repositório PST encapsulado](using-a-wrapped-pst-store-provider.md)
  
[DesLigamento de um provedor de repositório PST encapsulado](shutting-down-a-wrapped-pst-store-provider.md)

