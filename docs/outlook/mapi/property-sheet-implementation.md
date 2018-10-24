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
ms.openlocfilehash: 9a0fad8fa20b2d94077f9fbdf8a3c595c0ab219e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580863"
---
# <a name="property-sheet-implementation"></a>Implementação da folha de propriedades

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma folha de propriedades é uma caixa de diálogo para exibir as propriedades de um objeto. As propriedades podem ser somente leitura, permitindo que o usuário apenas para exibi-los, ou leitura/gravação, permitindo que o usuário faça alterações. Uma folha de propriedades contém uma ou mais janelas sobrepostas filho chamadas páginas. Cada página contém o controle do windows para configurar um grupo de propriedades relacionadas. Os usuários navegar pelas páginas selecionando uma guia que traz a página correspondente para o primeiro plano da folha de propriedades.
  
Provedores de serviços devem implementar uma folha de propriedades que exibe um conjunto mínimo de propriedades relacionadas a configuração no serviço de mensagem. Se você permitir essas propriedades do serviço de mensagem a ser alterado, você pode permitir que os usuários do cliente de aplicativos, como o painel de controle, para fazer as alterações ou implementar as alterações programaticamente. A implementação de folhas de propriedades para exibir e editar outros tipos de propriedades é opcional. 
  
Normalmente, você precisará de uma folha de propriedades de exibição nas seguintes situações:
  
- Quando um cliente chama o método de [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) do objeto seu status. 
    
- Quando o MAPI chama o método de logon do objeto do provedor.
    
- Quando o MAPI chama a função do ponto de entrada para o serviço de mensagem do seu provedor.
    
Provedores de transporte também implementam folhas de propriedades para exibir as propriedades relacionadas às opções de mensagem e folhas de propriedades para exibir e editar informações detalhadas sobre as mensagens de usuários e listas de distribuição, pesquisa avançada de implementar provedores do catálogo de endereços critérios e modelos para inserir novos usuários.
  
Você pode usar uma das três técnicas a seguir para criar uma folha de propriedades:
  
- Manualmente, como faria com qualquer caixa de diálogo.
    
- Usando o controle comuns da folha de propriedade fornecido no SDK do Windows.
    
- Usando uma MAPI exibe a tabela.
    
Provedores devem escolher a última opção (criar uma folha de propriedades usando uma tabela de exibição). Esta é a opção mais simples, pois elimina a necessidade de trabalhar com a interface de usuário do Windows. 
  
Para implementar uma folha de propriedades construída a partir de uma tabela de exibição para as propriedades do serviço de mensagem, use o procedimento a seguir:
  
1. Chame [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) para abrir uma seção no perfil atual. Passe o [MAPIUID](mapiuid.md) ou NULL para abrir a seção de perfil do seu provedor. 
    
2. Chame [CreateIProp](createiprop.md) para criar um objeto de dados de propriedade. 
    
3. Chame o método de [IMAPIProp::CopyTo](imapiprop-copyto.md) da seção perfil para copiar todas as propriedades da seção para o objeto de dados de propriedade. 
    
4. Crie uma tabela de exibição com a criação de uma ou mais estruturas [DTPAGE](dtpage.md) que descrevem os controles para que ele apareça na folha de propriedades e chamar a função [BuildDisplayTable](builddisplaytable.md) ou por meio da implementação código personalizado. 
    
5. Chame [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) para exibir uma folha de propriedades que tem as propriedades copiadas. Passe um ponteiro para o objeto de dados de propriedade como o parâmetro _lpConfigData_ e um ponteiro para a tabela de exibição como o parâmetro _lpDisplayTable_ . Se você quiser substituir o modo de acesso padrão para essa folha de propriedades, não defina o sinalizador DT_EDITABLE para cada controle na tabela de exibição que representa uma propriedade somente leitura. 
    
6. Quando todas as alterações são feitas na folha de propriedades, chame o método de **IMAPIProp::CopyTo** do objeto de dados de propriedade para copiar as propriedades alteradas voltar para a seção de perfil. 
    
Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md). 
  
Para obter informações detalhadas sobre tabelas de exibição, consulte [Exibir implementação da tabela](display-table-implementation.md). 
  
Para obter informações sobre como implementar um controle, consulte [Implementação do objeto de controle](control-object-implementation.md).
  
Para recuperar o índice de um controle que um usuário seleciona em uma caixa de listagem da tabela de exibição, aguarde até que o usuário clica **Okey** ou em **Aplicar**. Neste ponto, o identificador de entrada do item selecionado será gravado novamente o [IMAPIProp: IUnknown](imapipropiunknown.md) interface como o valor da propriedade especificada pelo membro **ulPRSetProperty** na estrutura [DTBLLBX](dtbllbx.md) . 
  
Se você precisar ser capaz de adicionar ou remover itens da sua caixa de listagem, usar uma tabela de exibição e o método [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) não funcionará. Em vez disso, considere a implementação de uma folha de propriedades com a API de folha de propriedade Win32 contida no arquivo Comdlg32. 
  
## <a name="see-also"></a>Confira também



[Provedores de serviços MAPI](mapi-service-providers.md)

