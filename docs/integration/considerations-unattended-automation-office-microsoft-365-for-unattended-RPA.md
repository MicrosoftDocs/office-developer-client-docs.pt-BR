---
title: Considerações sobre a automação autônoma do Office no Microsoft 365 para o ambiente do RPA autônomo
ms.date: 03/30/2020
ms.audience: Developer
localization_priority: Normal
description: Considerações sobre a automação autônoma do Office no Microsoft 365 para o ambiente do RPA autônomo.
ms.openlocfilehash: 576217fc85f2980a6d2451e3f930296ea4c11a56
ms.sourcegitcommit: 007aa2ceb4f569201c3f4372de5c83b6c61f8875
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2020
ms.locfileid: "43103044"
---
# <a name="considerations-for-unattended-automation-of-office-in-the-microsoft-365-for-unattended-rpa-environment"></a>Considerações sobre a automação autônoma do Office no Microsoft 365 para o ambiente do RPA autônomo

Embora o Microsoft 365 para RPA autônomo forneça uma licença que permite a automação do Office sem nenhum usuário presente, todas as versões atuais do Office foram projetadas e testadas para executar como produtos de usuário final em uma estação de trabalho cliente com um usuário presente para interagir com a interface do aplicativo. Comportamentos inesperados resultantes do uso de aplicativos sem um usuário presente não são defeitos. Se quiser executar o Office nessa configuração, você deve estar preparado para considerar esses comportamentos inesperados na lógica do aplicativo.

Este artigo descreve algumas das considerações da automação autônoma do Office para ajudá-lo se você usar essa abordagem. No entanto, observe que o uso do Office nessa configuração é estritamente "como está" e deve considerar esses comportamentos inesperados. As informações fornecidas aqui não são exaustivas e não garantem a resolução de todos os problemas de todos os clientes. Recomendamos que você teste sua solução exaustivamente antes de implantar o.

## <a name="common-problems-in-unattended-automation"></a>Problemas comuns na automação autônoma

Se você quiser usar o Office sem um usuário presente, esteja ciente das seguintes áreas nas quais o Office pode se comportar de forma diferente do esperado. Para que sua solução seja executada com êxito, ela deve resolver esses problemas e minimizar seus efeitos tanto quanto possível. Considere esses problemas cuidadosamente ao criar seu aplicativo.

### <a name="interactive-ui-elements"></a>Elementos de interface do usuário interativa

Os aplicativos do Office presumem que estão sendo executados interativamente. Se ocorrer um erro inesperado ou se um parâmetro não especificado for necessário para concluir uma função, o Office será projetado para solicitar ao usuário uma caixa de diálogo que pergunte ao usuário como eles desejam proceder. Na automação autônoma, isso pode fazer com que o aplicativo apareça como "travar" à medida que o aplicativo é interrompido até receber essa entrada. Se você estiver automatizando o Office por meio de suas APIs públicas, poderá suprimir muitos desses alertas Configurando propriedades como [Application. DisplayAlerts](https://docs.microsoft.com/office/vba/api/word.application.displayalerts) e [Application. AutomationSecurity](https://docs.microsoft.com/office/vba/api/word.application.automationsecurity) adequadamente. O código deve ser projetado para identificar e processar alertas de bloqueio a qualquer momento.

### <a name="user-identity"></a>Identidade do usuário

Os aplicativos do Office exigem uma identidade de usuário quando os aplicativos são executados, mesmo quando o aplicativo é iniciado por meio da automação. Essa identidade de usuário pode causar qualquer um dos seguintes:

- A presença de interface do usuário de entrada adicional que deve ser tratada.
- Arquivos que não podem ser abertos e/ou editados com base em permissões de acesso por usuário.
- Alterações inesperadas para os metadados do arquivo (por exemplo, determinadas propriedades de arquivo serão atualizadas com base na identidade da identidade do usuário da instância de aplicativo automatizada).

Várias abordagens podem ajudar a reduzir esses problemas; por exemplo, executando o [Inspetor de documento](https://docs.microsoft.com/office/vba/library-reference/concepts/using-the-document-inspector) para remover metadados. Considere se essas abordagens são apropriadas com base em seu cenário.

### <a name="server-side-security"></a>Segurança no servidor

Ao executar o Office autônomo e o processamento de conteúdo de arquivo arbitrário, nenhuma proteção adicional específica nesse ambiente estará disponível para impedir que as macros armazenadas nesses arquivos sejam carregadas e executadas. O Office não protege você contra a execução acidental de macros do código ou a inicialização de outro servidor que possa executar macros. Você pode usar propriedades como [Application. AutomationSecurity](https://docs.microsoft.com/office/vba/api/word.application.automationsecurity) para reduzir esse risco, mas você deve garantir que você esteja apenas carregando conteúdo confiável.

Além disso, o Office usa vários componentes (como Simple MAPI, WinInet e MSDAIPP) que podem armazenar em cache as informações de autenticação do cliente para agilizar o processamento. Quando o Office está sendo automatizado no servidor e processando vários arquivos, se as informações de autenticação forem armazenadas em cache para essa sessão, um cliente poderá usar as credenciais armazenadas em cache de outro cliente. Portanto, o cliente pode obter permissões de acesso não concedidas por meio da representação de outros usuários.

### <a name="ui-changes"></a>Alterações na interface do usuário

Os elementos da interface do usuário do Office são amplamente estáveis, mas o local específico de qualquer elemento de interface do usuário não é garantido e pode ser alterado conforme o design do produto evolui para incorporar os comentários do usuário e atender às necessidades do cliente. A lógica de qualquer automação deve considerar isso. Essas alterações podem resultar em alterações de nome de guia de grupo ou de botão, movimentação de comandos entre guias, adição de novas guias ou remoção de comandos em alinhamento com as políticas de substituição de recursos. Essas alterações podem ocorrer na interface do usuário, bem como nas informações de acessibilidade fornecidas pelo aplicativo, pois essas informações são modificadas para melhorar a usabilidade e a conta para comentários contínuos do cliente e podem ser implantadas para diferentes usuários em momentos diferentes.

Mesmo sem alterações de produto, as diferenças entre ambientes de sistema (como tamanho de tela/resolução/DPI) podem resultar em alterações no local dos itens na tela. Qualquer abordagem que se baseia em coordenadas de tela para simular a entrada do usuário deve considerar essas alterações e se adaptar de acordo.

### <a name="single-threading"></a>Segmentação única

Os aplicativos do Office são aplicativos baseados em STA e não reentrante que são projetados para fornecer funcionalidades diversas, mas intensivamente, para um único cliente. Os aplicativos usam recursos globais, como arquivos mapeados de memória, suplementos globais ou modelos e servidores de automação compartilhados. Isso pode limitar o número de instâncias que podem ser executadas simultaneamente e podem levar a condições de corrida se os aplicativos estiverem configurados em um ambiente de vários clientes. Se você planeja executar mais de uma instância de qualquer aplicativo do Office, você deve planejar isolá-los no nível da máquina virtual para garantir a estabilidade da solução resultante.

### <a name="resiliency-and-stability"></a>Resiliência e estabilidade

Mesmo com as considerações acima, se os aplicativos forem automatizados de maneiras de simular a entrada do usuário ou para os comprimentos da sessão que excederem drasticamente o uso interativo, poderão encontrar problemas que não estão presentes quando executado de forma interativa. As soluções que utilizam o Office nesse contexto devem criar mecanismos de forma proativa para monitorar o estado do aplicativo e reiniciá-los (e/ou a máquina virtual em que estão sendo executados) se/conforme necessário.

## <a name="suggested-alternatives"></a>Alternativas sugeridas

A Microsoft recomenda algumas alternativas que não exigem que o Office seja instalado e execute o lado do servidor e que possa realizar tarefas comuns de forma mais eficiente e mais rápida do que a automação nessa configuração. Antes de envolver o Office como um componente do lado do servidor em seu projeto, considere as alternativas.

### <a name="microsoft-graph"></a>Microsoft Graph

A API do Microsoft Graph fornece acesso aos serviços, aos dados e à inteligência que estão disponíveis para usuários e soluções como parte da nuvem da Microsoft, incluindo vários serviços que dão suporte às necessidades de automação autônoma: acesso a emails de usuários/calendário/contatos/arquivos, conversão de documentos, cálculo de pasta de trabalho do Excel e muito mais. Esses serviços foram projetados para uso autônomo e acesso de alta escala e utilizam uma sintaxe de API RESTful padrão. Para obter mais informações sobre o Microsoft Graph e como usá-lo para trabalhar com os dados dos usuários, visite o seguinte:

- [Visão geral do Microsoft Graph](https://docs.microsoft.com/graph/overview) 
- [Introdução ao Microsoft Graph](https://developer.microsoft.com/graph/get-started)
- [Baixar um arquivo em outro formato](https://docs.microsoft.com/graph/api/driveitem-get-content-format?view=graph-rest-1.0&tabs=http) (conversão de arquivo)
- [Trabalhando com o Excel no Microsoft Graph](https://docs.microsoft.com/graph/api/resources/excel?view=graph-rest-1.0) (detalhes da pasta de trabalho)

### <a name="open-xml-file-formats"></a>Formatos de arquivo Open XML

Muitas tarefas de automação envolvem a criação ou edição de documentos. O Office oferece suporte a formatos de arquivo Open XML que permitem que os desenvolvedores criem, editem, leiam e transformem conteúdo de arquivo usando as tecnologias XML e ZIP padrão, definidas no ISO 29500 International Standard. Esses formatos de arquivo podem ser manipulados por meio de ferramentas ZIP/XML, incluindo o namespace System.IO.Package.IO na estrutura do Microsoft .NET 3. x. A edição direta dos formatos de arquivo é o método recomendado e com suporte para lidar com alterações em arquivos do Office de um serviço.

A Microsoft fornece um SDK para manipular formatos de arquivo Open XML da estrutura do .NET 3. x. Para obter mais informações sobre o SDK e como usar o SDK para criar ou editar arquivos Open XML, visite o seguinte:

- [Noções básicas sobre os formatos de arquivo XML abertos](https://docs.microsoft.com/office/open-xml/understanding-the-open-xml-file-formats)
- [Bem-vindo ao Open XML SDK 2,5 para Office](https://docs.microsoft.com/office/open-xml/open-xml-sdk)
