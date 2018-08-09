---
title: Aplicando um modelo de provedor de amostra
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: da487569-f2f0-404c-b944-38ed1c1b82bb
description: 'Os modelos de provedor do Outlook Social Connector (OSC) de amostra proporcionam uma estrutura para implementar um provedor OSC. '
ms.openlocfilehash: 2388da58690e1870434c576bfa68649937156c54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770815"
---
# <a name="applying-a-sample-provider-template"></a>Aplicando um modelo de provedor de amostra

Os modelos de provedor do Outlook Social Connector (OSC) de amostra proporcionam uma estrutura para implementar um provedor OSC. Os modelos de provedor estão disponíveis no C++, c# e Visual Basic. Esses modelos são apenas um ponto de partida para o desenvolvimento de provedor; os modelos não atendem escrever o código de implementação do provedor e a criação de um pacote de instalação para o provedor. O procedimento a seguir mostra como aplicar um modelo de provedor do OSC quando começar a desenvolver um provedor.
  
### <a name="to-apply-an-osc-provider-template"></a>Para aplicar um modelo de provedor do OSC

1. No menu **Iniciar** , clique com o botão **Microsoft Visual Studio 2010** e clique no comando **Executar como administrador** . Quando solicitado, clique em **Sim** para executar o Visual Studio como administrador. 
    
2. Altere o nome do projeto e o namespace do modelo para seus identificadores de nome e o namespace do projeto.
    
3. Modifica a classe **AssemblyInfo** para especificar as informações de assembly apropriado. 
    
4. Implementar os membros de interface marcados como **tarefas pendentes** e adicione mais dependências e referências, conforme necessário. 
    
5. Compile o projeto.
    
6. Certifique-se de que o assembly do provedor ProgID está listado como uma chave em `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.
    
7. Para distribuir o projeto de instalação, crie um projeto de instalação no Visual Studio ou uma ferramenta de configuração de sua escolha.
    
8. Seu projeto de instalação deve concluir o registro COM para o seu assembly e também criar a chave ProgID conforme listado na etapa 5.
    
## <a name="see-also"></a>Confira também

- [Baixando os exemplos](downloading-the-samples.md)
- [Modelos de amostra do OSC](osc-sample-templates.md)

