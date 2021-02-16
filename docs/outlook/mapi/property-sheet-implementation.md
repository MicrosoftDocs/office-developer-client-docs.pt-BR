---
title: Implementação da Folha de Propriedades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f3475206-0237-4b5b-8efd-abd5d5e0b6c3
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3f1c6497a182231645691f669d8900d33b495503
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430046"
---
# <a name="property-sheet-implementation"></a>Implementação da Folha de Propriedades

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma folha de propriedades é uma caixa de diálogo para exibir as propriedades de um objeto. As propriedades podem ser somente leitura, permitindo que o usuário só as veja ou leitura/gravação, permitindo que o usuário faça alterações. Uma folha de propriedades contém uma ou mais janelas filho sobrepostas chamadas páginas. Cada página contém janelas de controle para definir um grupo de propriedades relacionadas. Os usuários navegam de página para página selecionando uma guia que traz a página correspondente para o primeiro plano da folha de propriedades.
  
Os provedores de serviços devem implementar uma folha de propriedades que exibe um conjunto mínimo de propriedades relacionadas à configuração no serviço de mensagens. Se você permitir que essas propriedades de serviço de mensagens sejam alteradas, poderá permitir que os usuários de aplicativos clientes, como o Painel de Controle, façam as alterações ou implementem as alterações programaticamente. Implementar folhas de propriedades para exibir e editar outros tipos de propriedades é opcional. 
  
Normalmente, você precisará exibir uma folha de propriedades nas seguintes situações:
  
- Quando um cliente chama o método [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) do objeto de status. 
    
- Quando o MAPI chama o método de logon do objeto do provedor.
    
- Quando o MAPI chama a função de ponto de entrada para o serviço de mensagens do provedor.
    
Os provedores de transporte também implementam folhas de propriedades para exibir propriedades relacionadas a opções de mensagem, e os provedores de agendamento de endereço implementam planilhas de propriedades para exibir e editar informações detalhadas sobre usuários de mensagens e listas de distribuição, critérios avançados de pesquisa e modelos para inserir novos usuários.
  
Você pode usar uma das três técnicas a seguir para criar uma folha de propriedades:
  
- Manualmente, como faria com qualquer caixa de diálogo.
    
- Usando o controle comum da folha de propriedades fornecido no SDK do Windows.
    
- Usando uma tabela de exibição MAPI.
    
Os provedores devem escolher a última opção (criar uma folha de propriedades usando uma tabela de exibição). Essa é a opção mais simples porque elimina a necessidade de trabalhar com a interface do usuário do Windows. 
  
Para implementar uma folha de propriedades criada a partir de uma tabela de exibição para as propriedades do serviço de mensagens, use o procedimento a seguir:
  
1. Chame [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) para abrir uma seção no perfil atual. Passe o [MAPIUID](mapiuid.md) ou NULL para abrir a seção de perfil do provedor. 
    
2. Chame [CreateIProp para](createiprop.md) criar um objeto de dados de propriedade. 
    
3. Chame o método [IMAPIProp::CopyTo](imapiprop-copyto.md) da seção de perfil para copiar todas as propriedades da seção para o objeto de dados de propriedade. 
    
4. Crie uma tabela de exibição criando uma ou mais estruturas [DTPAGE](dtpage.md) que descrevam os controles a ser exibidos na folha de propriedades e chamando a função [BuildDisplayTable](builddisplaytable.md) ou implementando código personalizado. 
    
5. Chame [IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) para exibir uma folha de propriedades que tenha as propriedades copiadas. Passe um ponteiro para o objeto de dados de propriedade como _o parâmetro lpConfigData_ e um ponteiro para a tabela de exibição como o _parâmetro lpDisplayTable._ Se você deseja substituir o modo de acesso padrão para essa folha de propriedades, não de definir o sinalizador DT_EDITABLE para cada controle na tabela de exibição que representa uma propriedade somente leitura. 
    
6. Quando todas as alterações foram feitas na folha de propriedades, chame o método **IMAPIProp::CopyTo** do objeto de dados de propriedade para copiar as propriedades alteradas de volta para a seção de perfil. 
    
Para uma visão geral das tabelas de exibição, consulte [Tabelas de Exibição.](display-tables.md) 
  
Para obter informações detalhadas sobre tabelas de exibição, consulte [Implementação de tabela de exibição.](display-table-implementation.md) 
  
Para obter informações sobre como implementar um controle, consulte [Implementação de objeto de controle.](control-object-implementation.md)
  
Para recuperar o índice de um controle que um usuário seleciona em uma caixa de listagem de tabela de **exibição,** aguarde até que o usuário clique em **OK** ou Aplicar. Neste ponto, o identificador de entrada do item selecionado é gravado de volta na interface [IMAPIProp : IUnknown](imapipropiunknown.md) como o valor da propriedade especificada pelo **membro ulPRSetProperty** na estrutura [DTBLLBX.](dtbllbx.md) 
  
Se você precisar adicionar ou remover itens da caixa de listagem, usar uma tabela de exibição e o método [IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) não funcionarão. Em vez disso, considere implementar uma folha de propriedades com a API da folha de propriedades Win32 contida no comdlg32.dll arquivo. 
  
## <a name="see-also"></a>Confira também



[Provedores de Serviços MAPI](mapi-service-providers.md)

