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
ms.openlocfilehash: eb51881aac6e1953a21686857944ba2a15d0dca2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356935"
---
# <a name="message-store-provider-sample"></a>Exemplo de provedor de repositório de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O exemplo de provedor de repositório PST encapsulado usa um provedor de arquivos de pastas particulares (PST) como back-end para armazenar dados. O provedor de repositório PST encapsulado deve ser usado em conjunto com a API de replicação. 
  
A API de replicação permite que você replique itens de um repositório de dados de back-end para um repositório de PST do Microsoft Outlook. Use a API de replicação para replicar os dados em um repositório PST dedicado e manter o controle do estado de sincronização. Para obter mais informações, consulte [sobre a API de replicação](about-the-replication-api.md).
  
A maioria das funções no provedor de repositório PST encapsulado de amostra passam seus argumentos diretamente para o provedor de PST subjacente. Determinadas funções exigem implementação especial e são descritos nos tópicos a seguir.
  
|||
|:-----|:-----|
|Arquivo  <br/> |WrpPST32. dll  <br/> |
|Diretório do código-fonte:  <br/> |SampleWrappedPSTStoreProvider\WrapPST  <br/> |
|Pacote  <br/> |C++  <br/> |
|Plataformas  <br/> |Microsoft Visual Studio 2008 para compilar para Windows Vista, Windows Server 2008, Windows XP SP2 e Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Recursos com suporte

Este exemplo suporta o Microsoft Outlook 2010 64-bit e foi revisado para o Outlook 2013. Consulte os tópicos a seguir para obter informações adicionais:
  
- [Sobre a API de replicação](about-the-replication-api.md)
    
- [Inicializando um provedor de repositório PST encapsulado](initializing-a-wrapped-pst-store-provider.md)
    
- [Fazer logon em um provedor de repositório PST encapsulado](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [Usando um provedor de repositório PST encapsulado](using-a-wrapped-pst-store-provider.md)
    
- [DesLigamento de um provedor de repositório PST encapsulado](shutting-down-a-wrapped-pst-store-provider.md)
    
 **Para instalar o exemplo de provedor de repositório PST encapsulado**
  
1. Para baixar o exemplo de provedor de PST encapsulado, confira [download dos exemplos de MAPI do Outlook](downloading-the-outlook-mapi-samples.md).
    
2. Localize a pasta onde você salvou os exemplos de MAPI do Outlook. Clique com o botão direito do mouse na pasta zip **OutlookMAPISamples número\<\> de versão** e clique em **extrair tudo**.
    
3. Clique em **procurar**, selecione o local onde deseja salvar o exemplo e, em seguida, clique em **extrair**.
    
4. Execute o Microsoft Visual Studio 2008.
    
5. No Microsoft Visual Studio 2008, clique em **arquivo**, selecione **abrir**e, em seguida, clique em **projeto/solução**.
    
6. Navegue até o local onde você salvou o exemplo, clique em **WrapPST. vcproj**e, em seguida, clique em **abrir**.
    
7. On the **Build** menu, click **Build Solution**.
    
8. Na caixa de diálogo **salvar arquivo como** , clique em **salvar**.
    
9. Na pasta onde você salvou o exemplo, clique com o botão direito do mouse no arquivo **install. bat** e, em seguida, clique em **Executar como administrador**.
    
10. Na caixa de diálogo **Controle de Conta de Usuário**, clique em **Continuar**.
    

