---
title: Aplicando um modelo de provedor de exemplo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: da487569-f2f0-404c-b944-38ed1c1b82bb
description: 'Os modelos de provedor do Outlook Social Connector (OSC) de exemplo lhe dão uma estrutura para implementar um provedor do OSC. '
ms.openlocfilehash: 10fb21ab640e298bc655b8cad554fae789e2ad47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425908"
---
# <a name="applying-a-sample-provider-template"></a>Aplicando um modelo de provedor de exemplo

Os modelos de provedor do Outlook Social Connector (OSC) de exemplo lhe dão uma estrutura para implementar um provedor do OSC. Os modelos de provedor estão disponíveis em C++, C# e Visual Basic. Esses modelos são apenas um ponto de partida para o desenvolvimento do provedor; os modelos não abordam a escrita do código de implementação para o provedor e a criação de um pacote de instalação para o provedor. O procedimento a seguir mostra como aplicar um modelo de provedor osC quando você começa a desenvolver um provedor.
  
### <a name="to-apply-an-osc-provider-template"></a>Para aplicar um modelo de provedor osC

1. No menu **Iniciar,** clique com o botão direito do mouse **no Microsoft Visual Studio 2010** e clique no comando Executar **como** administrador. Quando solicitado, clique em **Sim para** executar o Visual Studio como administrador. 
    
2. Altere o nome do projeto e o namespace no modelo para os identificadores de namespace e nome do projeto.
    
3. Modifique **a classe AssemblyInfo** para especificar as informações de assembly apropriadas. 
    
4. Implemente os membros da interface marcados **como To-Do** e adicione mais dependências e referências, conforme necessário. 
    
5. Compile o projeto.
    
6. Verifique se o ProgID do assembly do provedor está listado como uma chave em  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` .
    
7. Para distribuir o projeto de instalação, crie um projeto de instalação no Visual Studio ou uma ferramenta de instalação de sua escolha.
    
8. Seu projeto de instalação deve concluir o registro COM para seu assembly e também criar a chave ProgID conforme listado na etapa 5.
    
## <a name="see-also"></a>Confira também

- [Baixando os exemplos](downloading-the-samples.md)
- [Modelos de exemplo do OSC](osc-sample-templates.md)

