---
title: Implementação da folha de propriedades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f3475206-0237-4b5b-8efd-abd5d5e0b6c3
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3f1c6497a182231645691f669d8900d33b495503
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328522"
---
# <a name="property-sheet-implementation"></a>Implementação da folha de propriedades

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma folha de propriedades é uma caixa de diálogo para exibir as propriedades de um objeto. As propriedades podem ser somente leitura, permitindo que o usuário apenas as visualize ou a leitura/gravação, permitindo que o usuário faça alterações. Uma folha de propriedades contém uma ou mais janelas filhas sobrepostas chamadas de páginas. Cada página contém janelas de controle para a configuração de um grupo de propriedades relacionadas. Os usuários navegam de uma página para a página selecionando uma guia que traz a página correspondente para o primeiro plano da folha de propriedades.
  
Os provedores de serviços devem implementar uma folha de propriedades que exibe um conjunto mínimo de propriedades relacionadas à configuração no serviço de mensagens. Se você permitir que essas propriedades do serviço de mensagens sejam alteradas, poderá permitir que os usuários de aplicativos cliente, como o painel de controle, façam as alterações ou implementem as alterações de forma programática. A implementação de folhas de propriedades para exibir e editar outros tipos de propriedades é opcional. 
  
Normalmente, você precisará exibir uma folha de propriedades nas seguintes situações:
  
- Quando um cliente chama o método [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) do objeto de status. 
    
- Quando MAPI chama o método de logon do objeto do provedor.
    
- Quando MAPI chama a função de ponto de entrada para o serviço de mensagens do provedor.
    
Os provedores de transporte também implementam folhas de propriedades para exibir propriedades relacionadas a opções de mensagens e provedores de catálogos de endereços implementam folhas de propriedades para exibir e editar informações detalhadas sobre usuários de mensagens e listas de distribuição, pesquisa avançada critérios e modelos para inserir novos usuários.
  
Você pode usar uma das três técnicas a seguir para criar uma folha de propriedades:
  
- Manualmente, como faria com qualquer caixa de diálogo.
    
- Usando o controle comum de folha de propriedades fornecido no Windows SDK.
    
- Usando uma tabela de exibição MAPI.
    
Os provedores devem escolher a última opção (criar uma folha de propriedades usando uma tabela de exibição). Esta é a opção mais simples porque elimina a necessidade de trabalhar com a interface de usuário do Windows. 
  
Para implementar uma folha de propriedades criada a partir de uma tabela de exibição para suas propriedades do serviço de mensagens, use o seguinte procedimento:
  
1. Chame [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) para abrir uma seção no perfil atual. Passe seu [MAPIUID](mapiuid.md) ou nulo para abrir a seção de perfil do provedor. 
    
2. Chame [CreateIProp](createiprop.md) para criar um objeto de dados de propriedade. 
    
3. Chame o método [IMAPIProp:: CopyTo](imapiprop-copyto.md) da seção de perfil para copiar todas as propriedades da seção para o objeto de dados de propriedade. 
    
4. Crie uma tabela de exibição criando uma ou mais estruturas [DTPAGE](dtpage.md) que descrevem os controles a serem exibidos na folha de propriedades e chamando a função [BuildDisplayTable](builddisplaytable.md) ou implementando código personalizado. 
    
5. Chamar [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) para exibir uma folha de propriedades que tenha as propriedades copiadas. Passe um ponteiro para o objeto de dados de propriedade como o parâmetro _lpConfigData_ e um ponteiro para a tabela de exibição como o parâmetro _lpDisplayTable_ . Se você deseja substituir o modo de acesso padrão para esta folha de propriedades, não defina o sinalizador DT_EDITABLE para cada controle na tabela de exibição que representa uma propriedade somente leitura. 
    
6. Quando todas as alterações tiverem sido feitas na folha de propriedades, chame o método **IMAPIProp:: CopyTo** do objeto de dados de propriedade para copiar as propriedades alteradas de volta para a seção perfil. 
    
Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md). 
  
Para obter informações detalhadas sobre como exibir tabelas, consulte [Exibir tabela de implementação](display-table-implementation.md). 
  
Para obter informações sobre a implementação de um controle, consulte [controle de implementação de objeto](control-object-implementation.md).
  
Para recuperar o índice de um controle selecionado por um usuário em uma caixa de listagem exibir tabela, aguarde até que o usuário clique em **OK** ou **aplicar**. Neste ponto, o identificador de entrada do item selecionado é gravado novamente na interface [IMAPIProp: IUnknown](imapipropiunknown.md) como o valor da propriedade especificada pelo membro **UlPRSetProperty** na estrutura [DTBLLBX](dtbllbx.md) . 
  
Se você precisar adicionar ou remover itens da sua caixa de listagem, usando uma tabela de exibição e o método [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) não funcionará. Em vez disso, considere a implementação de uma folha de propriedades com a API de folha de propriedades do Win32 contida no arquivo Comdlg32. dll. 
  
## <a name="see-also"></a>Confira também



[Provedores de serviço MAPI](mapi-service-providers.md)

