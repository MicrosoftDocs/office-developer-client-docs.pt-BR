---
title: Exemplo de provedor de armazenamento de mensagens
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f1e4077b-7a95-440d-a326-a8dc9cdab4fe
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: eb51881aac6e1953a21686857944ba2a15d0dca2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436864"
---
# <a name="message-store-provider-sample"></a>Exemplo de provedor de armazenamento de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O Provedor de Armazenamento PST com Conteúdo de Exemplo usa um provedor de arquivos de Pastas Particulares (PST) como back-end para armazenar dados. O provedor de armazenamento PST empacotado deve ser usado junto com a API de Replicação. 
  
A API de Replicação permite replicar itens de um repositório de dados back-end para um repositório PST do Microsoft Outlook. Use a API de Replicação para replicar os dados em um armazenamento PST dedicado e acompanhar o estado de sincronização. Para obter mais informações, consulte [Sobre a API de replicação.](about-the-replication-api.md)
  
A maioria das funções no Provedor de Armazenamento PST com Fim de Exemplo passa seus argumentos diretamente para o provedor de PST subjacente. Determinadas funções exigem implementação especial e são descritas nos tópicos a seguir.
  
|||
|:-----|:-----|
|Executável:  <br/> |WrpPST32.dll  <br/> |
|Diretório do código-fonte:  <br/> |SampleWrappedPSTStoreProvider\WrapPST  <br/> |
|Idioma:  <br/> |C++  <br/> |
|Plataformas:  <br/> |Microsoft Visual Studio 2008 para compilar para Windows Vista, Windows Server 2008, Windows XP SP2 e Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Recursos com suporte

Este exemplo dá suporte ao Microsoft Outlook 2010 de 64 bits e agora foi revisado para o Outlook 2013. Consulte os tópicos a seguir para obter informações adicionais:
  
- [Sobre a API de replicação](about-the-replication-api.md)
    
- [Inicializando um provedor de armazenamento PST empacotado](initializing-a-wrapped-pst-store-provider.md)
    
- [Logondo em um provedor de armazenamento PST empacotado](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [Usando um provedor de armazenamento PST empacotado](using-a-wrapped-pst-store-provider.md)
    
- [Desligar um provedor de armazenamento PST empacotado](shutting-down-a-wrapped-pst-store-provider.md)
    
 **Para instalar o Sample Wrapped PST Store Provider**
  
1. Para baixar o Exemplo de Provedor de PST com Fim, consulte [Baixando os exemplos de MAPI do Outlook.](downloading-the-outlook-mapi-samples.md)
    
2. Localize a pasta onde você salvou os exemplos de MAPI do Outlook. Clique com o botão direito do mouse na pasta zip do número de versão do **OutlookMAPISamples \< \>** e clique em **Extrair Tudo.**
    
3. Clique **em** Procurar, selecione o local onde deseja salvar o exemplo e clique em **Extrair.**
    
4. Execute o Microsoft Visual Studio 2008.
    
5. No Microsoft Visual Studio 2008, clique em **Arquivo,** selecione **Abrir** e clique em **Projeto/Solução.**
    
6. Navegue até o local onde você salvou o exemplo, clique em **WrapPST.vcproj** e clique em **Abrir**.
    
7. On the **Build** menu, click **Build Solution**.
    
8. Na caixa **de diálogo Salvar Arquivo como,** clique em **Salvar.**
    
9. Na pasta onde você salvou o exemplo, clique com o botão direito do mouse no arquivo **install.bat** e clique em **Executar como administrador.**
    
10. Na caixa de diálogo **Controle de Conta de Usuário**, clique em **Continuar**.
    

