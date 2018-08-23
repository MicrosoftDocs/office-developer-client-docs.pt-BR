---
title: Exemplo de provedor de repositório de mensagens
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f1e4077b-7a95-440d-a326-a8dc9cdab4fe
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 25c606531aa9a7436306a1b87c32aab49fd975db
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593911"
---
# <a name="message-store-provider-sample"></a>Exemplo de provedor de repositório de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O provedor de repositórios de PST quebrado automaticamente amostra usa um provedor de pastas particulares (. PST) do arquivo como back-end para armazenar os dados. O provedor de repositórios de PST com quebra deve ser usado em conjunto com a API de replicação. 
  
A API de replicação permite que você replique os itens de um repositório de dados back-end em um repositório de PST do Microsoft Outlook. Você pode usar a API de replicação para replicar os dados para um repositório de PST dedicado e controlar o estado de sincronização. Para obter mais informações, consulte [Sobre o API de replicação](about-the-replication-api.md).
  
A maioria das funções do provedor de armazenamento do exemplo quebradas PST passa seus argumentos diretamente para o provedor de PST subjacente. Determinadas funções exigem implementação especial e são descritas nos tópicos a seguir.
  
|||
|:-----|:-----|
|Executável:  <br/> |WrpPST32.dll  <br/> |
|Diretório de origem do código:  <br/> |SampleWrappedPSTStoreProvider\WrapPST  <br/> |
|Idioma:  <br/> |C++  <br/> |
|Plataformas:  <br/> |Microsoft Visual Studio 2008 para compilar para Windows Vista, Windows Server 2008, Windows XP SP2 e Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Recursos compatíveis

Esta amostra suporta o Microsoft Outlook 2010 64-bit e agora foi revisada para o Outlook 2013. Consulte os tópicos a seguir para obter informações adicionais:
  
- [Sobre a API de replicação](about-the-replication-api.md)
    
- [Iniciar um provedor do repositório PST encapsulado](initializing-a-wrapped-pst-store-provider.md)
    
- [Fazer logon em um provedor do repositório PST encapsulado](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [Usar um provedor do repositório PST encapsulado](using-a-wrapped-pst-store-provider.md)
    
- [Desativar um provedor do repositório PST encapsulado](shutting-down-a-wrapped-pst-store-provider.md)
    
 **Para instalar o provedor de armazenamento do exemplo quebradas PST**
  
1. Para baixar o provedor de PST quebrado automaticamente da amostra, consulte [Baixando as amostras de MAPI do Outlook](downloading-the-outlook-mapi-samples.md).
    
2. Localize a pasta onde você salvou as amostras de MAPI do Outlook. Com o botão direito do **OutlookMAPISamples -\<número da versão\> ** zip pasta e clique em **Extrair tudo**.
    
3. Clique em **Procurar**, selecione o local onde deseja salvar a amostra e, em seguida, clique em **extrair**.
    
4. Execute o Microsoft Visual Studio 2008.
    
5. No Microsoft Visual Studio 2008, clique em **arquivo**, selecione **Abrir**e, em seguida, clique em **Project/Solution**.
    
6. Navegue até o local onde você salvou a amostra, clique em **WrapPST.vcproj**e, em seguida, clique em **Abrir**.
    
7. On the **Build** menu, click **Build Solution**.
    
8. Na caixa de diálogo **Salvar arquivo como** , clique em **Salvar**.
    
9. Na pasta onde você salvou a amostra, com o botão direito do arquivo **Install. bat** e clique em **Executar como administrador**.
    
10. Na caixa de diálogo **Controle de conta de usuário** , clique em **continuar**.
    

