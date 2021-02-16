---
title: Considerações sobre a automação autônoma do Office no Microsoft 365 para o ambiente RPA autônomo
ms.date: 03/30/2020
ms.audience: Developer
localization_priority: Normal
description: Considerações sobre a automação autônoma do Office no Microsoft 365 para o ambiente RPA autônomo.
ms.openlocfilehash: 576217fc85f2980a6d2451e3f930296ea4c11a56
ms.sourcegitcommit: 007aa2ceb4f569201c3f4372de5c83b6c61f8875
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2020
ms.locfileid: "43103044"
---
# <a name="considerations-for-unattended-automation-of-office-in-the-microsoft-365-for-unattended-rpa-environment"></a>Considerações sobre a automação autônoma do Office no Microsoft 365 para o ambiente RPA autônomo

Embora o Microsoft 365 para RPA autônomo fornece uma licença que permite a automação do Office sem nenhum usuário presente, todas as versões atuais do Office foram projetadas e testadas para executar como produtos de usuário final em uma estação de trabalho cliente com um usuário presente para interagir com a interface do aplicativo. Comportamentos inesperados resultantes do uso de aplicativos sem um usuário presente não são defeitos. Se quiser executar o Office nessa configuração, você deve estar preparado para levar em conta esses comportamentos inesperados na lógica do aplicativo.

Este artigo descreve algumas das considerações para a automação autônoma do Office para ajudá-lo se você usar essa abordagem. No entanto, observe que o uso do Office nessa configuração é estritamente "COMO ESTÁ" e deve levar em conta esses comportamentos inesperados. As informações fornecidas aqui não são exaustivas e não são garantidas para resolver todos os problemas de todos os clientes. Recomendamos que você teste sua solução exaustivamente antes de implantar.

## <a name="common-problems-in-unattended-automation"></a>Problemas comuns na automação autônoma

Se você quiser usar o Office sem um usuário presente, esteja ciente das seguintes áreas nas quais o Office pode se comportar de maneira diferente do esperado. Para que sua solução seja executado com êxito, ela deve resolver esses problemas e minimizar os efeitos o máximo possível. Considere esses problemas cuidadosamente ao criar seu aplicativo.

### <a name="interactive-ui-elements"></a>Elementos interativos da interface do usuário

Os aplicativos do Office presumem que eles estão sendo executados interativamente. Se ocorrer um erro inesperado ou se for necessário um parâmetro não especificado para concluir uma função, o Office foi projetado para solicitar ao usuário uma caixa de diálogo que pergunta ao usuário como ele deseja continuar. Na automação autônoma, isso pode fazer com que o aplicativo pareça "travado" à medida que o aplicativo para até receber essa entrada. Se você estiver automatizando o Office por meio de suas APIs públicas, poderá suprimir muitos desses alertas configurando propriedades como [Application.DisplayAlerts](https://docs.microsoft.com/office/vba/api/word.application.displayalerts) e [Application.AutomationSecurity](https://docs.microsoft.com/office/vba/api/word.application.automationsecurity) adequadamente. Seu código deve ser projetado para identificar e processar alertas de bloqueio a qualquer momento.

### <a name="user-identity"></a>Identidade do usuário

Os aplicativos do Office exigem uma identidade de usuário quando os aplicativos são executados, mesmo quando o aplicativo é iniciado via automação. Essa identidade de usuário pode causar um ou todos os seguintes:

- A presença de interface do usuário de login adicional que deve ser manipulada.
- Arquivos que não podem ser abertos e/ou editados com base em permissões de acesso por usuário.
- Alterações inesperadas nos metadados do arquivo (por exemplo, determinadas propriedades de arquivo serão atualizadas com base na identidade do usuário da instância automatizada do aplicativo).

Várias abordagens podem ajudar a atenuar esses problemas; por exemplo, executar o [Inspetor de Documento](https://docs.microsoft.com/office/vba/library-reference/concepts/using-the-document-inspector) para remover metadados. Considere se essas abordagens são apropriadas com base em seu cenário.

### <a name="server-side-security"></a>Segurança do lado do servidor

Ao executar o conteúdo arbitrário de arquivo autônomo do Office e processar, nenhuma proteção adicional específica desse ambiente estará disponível para impedir que macros armazenadas nesses arquivos sejam carregadas e em execução. O Office não protege você de executar macros involutionamente do seu código ou de iniciar outro servidor que possa executar macros. Você pode usar propriedades como [Application.AutomationSecurity](https://docs.microsoft.com/office/vba/api/word.application.automationsecurity) para reduzir esse risco, mas deve garantir que está carregando apenas conteúdo confiável.

Além disso, o Office usa muitos componentes (como SIMPLE MAPI, WinInet e MSDAIPP) que podem armazenar em cache as informações de autenticação do cliente para acelerar o processamento. Quando o Office está sendo automatizado no lado do servidor e processando vários arquivos, se as informações de autenticação foram armazenadas em cache para essa sessão, um cliente pode usar as credenciais armazenadas em cache de outro cliente. Portanto, o cliente pode obter permissões de acesso não concedidas, representando outros usuários.

### <a name="ui-changes"></a>Alterações na interface do usuário

Os elementos de interface do usuário no Office são amplamente estáveis, mas o local específico de qualquer elemento da interface do usuário não é garantido e pode mudar à medida que o design do produto evolui para incorporar comentários do usuário e atender às necessidades do cliente. A lógica de qualquer automação deve levar em conta isso. Essas alterações podem resultar em alterações de nomeação de botão ou guia de grupo, movimento de comandos entre guias, adição de novas guias ou a remoção de comandos em alinhamento com nossas políticas de preteração de recursos. Essas alterações podem ocorrer na interface do usuário, bem como nas informações de acessibilidade fornecidas pelo aplicativo, pois essas informações são modificadas para melhorar a usabilidade e contabilizar comentários contínuos dos clientes e podem ser disponibilizadas para usuários diferentes em momentos diferentes.

Mesmo sem alterações no produto, as diferenças entre ambientes do sistema (como tamanho/resolução/DPI da tela) podem resultar em alterações na localização dos itens na tela. Qualquer abordagem que depende de coordenadas de tela para simular a entrada do usuário deve considerar essas alterações e adaptar-se de acordo.

### <a name="single-threading"></a>Threading único

Os aplicativos do Office são aplicativos não reentráveis e baseados em STA projetados para fornecer funcionalidade diversificada, mas que utiliza muitos recursos para um único cliente. Os aplicativos usam recursos globais, como arquivos mapeados na memória, modelos ou complementos globais e servidores de automação compartilhados. Isso pode limitar o número de instâncias que podem ser executados simultaneamente e podem levar a condições de corrida se os aplicativos estão configurados em um ambiente multicliente. Se você planeja executar mais de uma instância de qualquer aplicativo do Office, planeje isolá-las no nível da máquina virtual para garantir a estabilidade da solução resultante.

### <a name="resiliency-and-stability"></a>Resiliência e estabilidade

Mesmo com as considerações acima, se os aplicativos são automatizados de maneiras que simulam a entrada do usuário ou para comprimentos de sessão que excedem drasticamente o uso interativo, eles podem encontrar problemas que não estão presentes quando executados interativamente. As soluções que utilizam o Office nesse contexto devem criar mecanismos de forma proativa para monitorar o estado do aplicativo e reiniciá-los (e/ou a máquina virtual na qual estão sendo executados) se/conforme necessário.

## <a name="suggested-alternatives"></a>Alternativas sugeridas

A Microsoft recomenda fortemente algumas alternativas que não exigem que o Office seja instalado e executado no lado do servidor, e que possam executar tarefas comuns com mais eficiência e mais rapidez do que a automação nessa configuração. Antes de envolver o Office como um componente do lado do servidor em seu projeto, considere alternativas.

### <a name="microsoft-graph"></a>Microsoft Graph

A API do Microsoft Graph fornece acesso aos serviços, dados e inteligência que estão disponíveis para usuários e soluções como parte da nuvem da Microsoft, incluindo muitos serviços que suportam as necessidades de automação autônoma: acesso ao email/calendário/contatos /arquivos dos usuários, conversão de documentos, cálculo da planilha do Excel e muito mais. Esses serviços são projetados para uso autônomo e acesso em alta escala e utilizam uma sintaxe de API RESTful padrão. Para obter mais informações sobre o Microsoft Graph e como usá-lo para trabalhar com os dados dos usuários, visite o seguinte:

- [Visão geral do Microsoft Graph](https://docs.microsoft.com/graph/overview) 
- [Introdução ao Microsoft Graph](https://developer.microsoft.com/graph/get-started)
- [Baixar um arquivo em outro formato (conversão](https://docs.microsoft.com/graph/api/driveitem-get-content-format?view=graph-rest-1.0&tabs=http) de arquivo)
- [Trabalhar com o Excel no Microsoft Graph](https://docs.microsoft.com/graph/api/resources/excel?view=graph-rest-1.0) (detalhes da planilha)

### <a name="open-xml-file-formats"></a>Formatos de arquivo Open XML

Muitas tarefas de automação envolvem a criação ou edição de documentos. O Office dá suporte a formatos de arquivo Open XML que permitem que os desenvolvedores criem, editem, leiam e transformem conteúdo de arquivo usando tecnologias XML e ZIP padrão, definidas no ISO 29500 International Standard. Esses formatos de arquivo podem ser manipulados por meio de qualquer ferramenta ZIP/XML, incluindo o namespace System.IO.Package.IO no Microsoft .NET 3.x Framework. A edição direta dos formatos de arquivo é o método recomendado e com suporte para manipular alterações em arquivos do Office de um serviço.

A Microsoft fornece um SDK para manipular formatos de arquivo Open XML do .NET 3.x Framework. Para obter mais informações sobre o SDK e como usar o SDK para criar ou editar arquivos Open XML, visite o seguinte:

- [Noções básicas sobre os formatos de arquivo XML abertos](https://docs.microsoft.com/office/open-xml/understanding-the-open-xml-file-formats)
- [Bem-vindo ao SDK 2.5 do Open XML para Office](https://docs.microsoft.com/office/open-xml/open-xml-sdk)
