---
title: Conceitos de segurança adicionais do formulário do InfoPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 77425a61-bf33-b3d8-442a-caee48e54a48
description: O modelo de segurança do Microsoft InfoPath baseia-se no modelo de segurança implementado pelo Internet Explorer. O modelo de segurança do Internet Explorer ajuda a proteger seu computador de operações perigosas usando níveis e zonas de segurança. Trabalhando em equipe com o modelo de segurança do Internet Explorer, o InfoPath oferece dois tipos de implantação de formulários que afetam como um formulário do InfoPath funciona nesse modelo de segurança.
ms.openlocfilehash: 00b0e306507db19f55059fba91277af1ad1714b9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303770"
---
# <a name="additional-infopath-form-security-concepts"></a>Conceitos de segurança adicionais do formulário do InfoPath

O modelo de segurança do Microsoft InfoPath baseia-se no modelo de segurança implementado pelo Internet Explorer. O modelo de segurança do Internet Explorer ajuda a proteger seu computador de operações perigosas usando níveis e zonas de segurança. Trabalhando em equipe com o modelo de segurança do Internet Explorer, o InfoPath oferece dois tipos de implantação de formulários que afetam como um formulário do InfoPath funciona nesse modelo de segurança.
  
- **Formulários baseados em URL** Esse método de implantação é o padrão quando um formulário é publicado do InfoPath para um servidor Web, uma biblioteca de formulários do SharePoint Foundation ou um compartilhamento de arquivos. Esses formulários são conhecidos como formulários baseados em URL, pois um usuário normalmente abre o formulário na URL em que ele é publicado. Essa URL é especificada no atributo **publishUrl** do elemento **xDocumentClass** no arquivo de definição de formulário (. xsf). Formulários baseados em URL são de área restrita, pois eles têm acesso restrito a recursos de sistema e outras possíveis áreas de risco. Um formulário baseado em URL tem o mesmo nível de permissões que uma página da Web aberta do mesmo local que o arquivo de modelo de formulário (. xsn).
    
- **Formulários baseados em URN** Esse método de implantação é para formulários que exigem acesso a recursos do sistema e outros recursos externos, como controles ActiveX e outros componentes de software. Você pode implantar formulários do InfoPath como formulários totalmente confiáveis. Esses formulários também são conhecidos como formulários baseados em URN porque, em vez de especificar o atributo **publishUrl**, eles especificam um Uniform Resource Name (URN) no atributo **nome** do elemento **xDocumentClass** no arquivo de definição de formulário (. xsf). Essa classe de formulário pode solicitar confiança total se o atributo **requireFullTrust** do elemento **xDocumentClass** for definido como `"yes"` no arquivo de definição de formulário (. xsf). Os formulários de URN devem ser registrados no computador cliente por um programa ou script.de instalação. Nesse caso, o formulário recebe as mesmas permissões que um aplicativo que está em execução no computador local. 
    
Juntamente com esses dois métodos de implantação de formulário, cada método e propriedade no modelo de objeto do InfoPath tem um nível de segurança que controla quando esse método ou propriedade pode ser chamado pelo script executado pelo formulário.
  
## <a name="understanding-infopath-integration-with-the-internet-explorer-security-model"></a>Noções básicas sobre a integração do InfoPath com o modelo de segurança do Internet Explorer

O Internet Explorer implementa zonas de segurança que permitem controlar o nível de acesso atribuído ao seu computador pelas páginas da Web que você abre. O InfoPath usa algumas dessas zonas para determinar o nível de acesso que formulários recebem aos recursos em seu computador. Por padrão, os formulários do InfoPath são executados em um local em cache que tem o acesso negado a recursos críticos do sistema. Os formulários que recebem acesso irrestrito a recursos de sistema são chamados de formulários totalmente confiáveis. Os formulários totalmente confiáveis são geralmente instalados e registrados usando um programa ou script de instalação ou são assinados digitalmente para que possam receber um nível superior de permissões.
  
Os formulários do InfoPath em cache são identificados pela URL ou pelo URN especificado no arquivo de definição de formulário (. xsf) do formulário. O tipo de identificação usado e o domínio (localização) do qual o modelo de formulário é aberto determina quais permissões de zona de segurança do Internet Explorer o formulário herdará. Formulários identificados por uma URL são armazenados em cache no computador do usuário, o que permite o uso offline desses formulários. Esses formulários baseados em URL herdam suas permissões de segurança e direitos de acesso específicos, como acesso entre domínios, das configurações de segurança do Internet Explorer aplicáveis à localização original do modelo de formulário. Os modelos de formulário armazenados em um servidor Web ou em um servidor executando o SharePoint Foundation são executados na Internet ou na zona da Intranet local, dependendo do domínio do servidor. Os formulários instalados que são identificados por um URN, por sua vez, herdam suas permissões da zona do Computador Local, que concede um nível de permissões parecidos com o de arquivos de aplicativo HTML (.hta).
  
Os formulários totalmente confiáveis são identificados por seu URN e pelo fato de o atributo **requireFullTrust** do elemento **xDocumentClass** no arquivo de definição de formulário (.xls) estar definido como `"yes"`. No InfoPath, depois que formulários totalmente confiáveis são instalados, eles são exibidos na guia **Novo** no modo de exibição Microsoft Office Backstage do editor do InfoPath. 
  
Para um discussão detalhada sobre como funcionam os formulários totalmente confiáveis e sobre como criá-los e implantá-los, consulte [Noções básicas sobre formulários totalmente confiáveis](understanding-fully-trusted-forms.md).
  
## <a name="trusting-installed-forms"></a>Confiando em formulários instalados

A capacidade de usar formulários confiáveis pode ser habilitada ou desabilitada em computadores individuais. Quando um computador está configurado para confiar nos formulários instalados, os usuários podem preencher formulários que exigem acesso a recursos do seu computador.
  
No editor do InfoPath, você pode configurar um computador para confiar em formulários instalados no modo de exibição Backstage clicando em **Opções**, **Central de Confiabilidade**, **configurações da Central de Confiabilidade** e marcando a caixa de seleção **Permitir que formulários totalmente confiáveis seja executados no meu computador** na aba **Fornecedores confiáveis** da caixa de diálogo **Central de Confiabilidade**. 
  
## <a name="using-security-features-in-infopath"></a>Usando recursos de segurança no InfoPath

O modelo de segurança do InfoPath ajuda a proteger os usuários contra as seguintes ameaças apresentadas por modelos criados maliciosamente:
  
- A possibilidade de divulgação de informações confidenciais do seu computador local ou de fontes de dados remotas.
    
- O uso mal-intencionado de controles ActiveX.
    
- O uso mal-intencionado de propriedades e métodos do modelo de objeto do InfoPath.
    
## <a name="cross-domain-data-access"></a>Acesso de dados entre domínios

Esta classe de cenários de risco de segurança é chamada de acesso de dados entre domínios.
  
O modelo de segurança do Internet Explorer que serve de base para o InfoPath oferece uma configuração chamada **Acessar fontes de dados entre domínios**. Por padrão, essa configuração desabilita o acesso entre domínios para formulários do InfoPath que residem na Internet e em Zonas de segurança de sites restritos. Ela solicita que o usuário permita ou não o acesso entre domínios para formulários do InfoPath que residem na zona de segurança da Intranet local e permite acesso entre domínios para formulários do InfoPath que residem nas zonas de **Sites confiáveis** ou da **Máquina Local**. 
  
## <a name="use-of-the-infopath-html-task-pane"></a>Uso do painel de tarefas HTML do InfoPath

O painel de tarefas HTML do InfoPath permite a renderização de páginas da Web, como arquivos. htm,. asp e. hta. As páginas referenciadas a partir de painéis de tarefas podem ser localizadas dentro ou fora do modelo de formulário. A única restrição quanto ao que pode ser referenciado de fora do modelo de formulário é que a página da Web deve estar no mesmo domínio que o modelo de formulário ou a zona de segurança em que o modelo reside deve conceder permissões de acesso entre domínios para carregar o painel de tarefas.
  
O painel de tarefas não expõe uma barra de endereços ou uma barra de status e, portanto, o usuário não tem como confirmar a localização da fonte para o painel de tarefas ou se esse local é acessado por um canal criptografado (https). Por esse motivo, você deve evitar usar o painel de tarefas para exibir ou inserir informações confidenciais. O painel de tarefas foi desenvolvido para exibir informações de ajuda dinâmicas e controles para navegar entre exibições e outros elementos de uma solução integrada. Além disso, a lógica de negócios e o script de um modelo de formulário no painel de tarefas podem interagir entre si. No entanto, essa interação é permitida apenas se o modelo de formulário e o painel de tarefas estiverem no mesmo domínio, o que ajuda a impedir que as informações sejam trocadas entre domínios.
  
## <a name="cross-domain-data-access-prompts"></a>Prompts de acesso de dados entre domínios

Se um modelo de formulário que requer acesso de dados entre domínios estiver localizado em uma zona de segurança definida para solicitar acesso de dados entre domínios (a configuração padrão para a zona da Intranet local), então o usuário será solicitado a permitir o acesso. A opção do usuário permanecerá durante o tempo restante em que o formulário estiver aberto. Se você precisa implantar modelos de formulário do InfoPath que exigem acesso de dados entre domínios, deve implantar esses modelos como formulários totalmente confiáveis ou disponibilizá-los em um servidor localizado na zona de segurança de Sites confiáveis para evitar que os usuários sejam solicitados a permitir o acesso. Os usuários não devem ser instruídos a diminuir o nível de segurança da zona da Intranet local para evitar esses prompts.
  
## <a name="forms-without-a-publishurl-attribute"></a>Formulários sem um atributo publishURL

Se o InfoPath carregar um modelo de formulário do computador local e ele apresentar um atributo **publishUrl** em branco ou o atributo estiver ausente, o formulário será colocado em uma zona de segurança mais restrita. Essa ação é realizada para reduzir a ameaça de um modelo de formulário mal-intencionado ser distribuído por email. Consequentemente, se o usuário salvar esse modelo de formulário em disco, ele não poderá ser executado com as permissões de um formulário que resida na zona da **Máquina Local**. 
  
## <a name="unsafe-activex-controls"></a>Controles ActiveX não seguros

O cenário mais comum para o uso mal-intencionado de controles ActiveX pode ocorrer se um autor usa o script com um controle ActiveX que fornece métodos para acessar o sistema de arquivos para recuperar arquivos pessoais e listas de senhas, excluir arquivos ou desabilitar o sistema do usuário. Um formulário do InfoPath só pode usar controles ActiveX por script no arquivo de script principal de um formulário (script. js) ou por script em um painel de tarefas. O InfoPath não permite que scripts executem controles ActiveX em modos de exibição do InfoPath.
  
O modelo de segurança do Internet Explorer que serve de base para o Microsoft InfoPath fornece uma configuração chamada **Inicializar e executar scripts de controles ActiveX marcados como não seguros**, que, por padrão, resulta nas seguintes ações para formulários do InfoPath ou painéis de tarefas que tentem inicializar e executar scripts de controles ActiveX marcados como não seguros para execução de scripts. 
  
|**Zona de segurança/Implantação**|**Ação**|
|:-----|:-----|
|Internet  <br/> |Desabilitado  <br/> |
|Intranet local  <br/> |Desabilitado  <br/> |
|Sites restritos  <br/> |Desabilitado  <br/> |
|Sites confiáveis  <br/> |Prompt  <br/> |
|Meu Computador  <br/> |Prompt  <br/> |
|Formulário totalmente confiável  <br/> |Habilitar  <br/> |
   
## <a name="malicious-use-of-the-infopath-object-model"></a>Uso mal-intencionado de modelo de objeto do InfoPath

Como no caso de controles ActiveX chamados por script, os métodos e propriedades do InfoPath chamados por código podem apresentar diferentes níveis de risco. Por exemplo, o método [SaveAs(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx) da classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) pode ser usado para gravar dados em qualquer local do sistema de arquivos. 
  
Para ajudar a proteger contra o uso malicioso de membros do modelo de objeto do InfoPath, o modelo de objeto do InfoPath implementa três níveis de segurança que determinam como e onde um membro específico do modelo de objeto pode ser usado. Há três níveis de segurança no modelo de objeto do InfoPath:
  
- **0** Membros do modelo de objeto que podem ser acessados sem restrições. Esses membros do modelo de objeto são seguros e, portanto, podem ser acessados sem restrições. 
    
- **2** Membros do modelo de objeto que podem ser acessados apenas por formulários executados no mesmo domínio que o formulário aberto atual ou por formulários que receberam permissões de acesso de dados entre domínios. Modelos de formulário restritos que chamam métodos de modelo de objeto de nível de segurança 2 só serão bem-sucedidos se estiveram acessando recursos contidos no próprio modelo de formulário. 
    
- **3** Membros do modelo de objeto que podem ser acessados apenas por formulários totalmente confiáveis. 
    
- Cada um dos tópicos referentes às propriedades e aos métodos na Referência do Modelo de Objeto do InfoPath contém uma seção de segurança que especifica o nível de segurança que se aplica a esse membro do modelo de objeto.
    
- O nível de segurança **1** está reservado para uso futuro. 
    
## <a name="summary"></a>Resumo

A tabela a seguir resume as permissões padrão para cada método de implantação de formulários no InfoPath. As permissões são baseadas na zona de segurança para o domínio de origem do modelo de formulário.
  
|**Zona de segurança**|**Implantação**|**Permissões padrão**|
|:-----|:-----|:-----|
||**Baseado em URL** <br/> |**Baseado em URN** <br/> |**ActiveX marcado como não seguro para execução de script** <br/> |**Acesso de dados entre domínios** <br/> |**Nível de segurança do modelo de objeto** <br/> |
|Sites restritos  <br/> |N/D  <br/> |N/D  <br/> |N/D  <br/> |N/D  <br/> |N/D  <br/> |
|Internet  <br/> |X  <br/> ||Desabilitar  <br/> |Desabilitar  <br/> |2   <br/> |
|Intranet local  <br/> |X  <br/> ||Desabilitar  <br/> |Prompt  <br/> |2   <br/> |
|Sites confiáveis  <br/> |X  <br/> ||Prompt  <br/> |Habilitar  <br/> |2   <br/> |
|Máquina Local  <br/> |X  <br/> |X  <br/> |Desabilitar  <br/> |Prompt  <br/> |2   <br/> |
|Formulário totalmente confiável  <br/> |X (assinado por um Fornecedor Confiável)  <br/> |X  <br/> |Habilitar  <br/> |Habilitar  <br/> |3   <br/> |
|Formulário totalmente confiável  <br/> ||X  <br/> |Habilitar  <br/> |Habilitar  <br/> |3   <br/> |
|Restrito  <br/> ||X  <br/> |Não ActiveX (exceto uma lista embutida em código limitada)  <br/> |Desabilitar  <br/> |2   <br/> |
|Restrito  <br/> |X  <br/> ||Não ActiveX (exceto uma lista embutida em código limitada)  <br/> |Desabilitar  <br/> |2   <br/> |
|Restrito  <br/> |X  <br/> |X  <br/> |Não ActiveX (exceto uma lista embutida em código limitada)  <br/> |Desabilitar  <br/> |2   <br/> |
   
Para saber mais sobre as diretrizes gerais de segurança ao desenvolver formulários, confira [Diretrizes de segurança para desenvolver formulários do InfoPath](security-guidelines-for-developing-infopath-forms.md).
  
## <a name="understanding-other-security-features"></a>Noções básicas sobre outros recursos de segurança

O InfoPath fornece outras medidas de segurança para formulários que incluem proteção de design do formulário por meio de assinaturas digitais, gerenciamento de determinadas operações de formulário como mesclagem e envio e confiabilidade de formulários instalados. As seções a seguir descrevem essas medidas de segurança e onde elas estão habilitadas no InfoPath.
  
## <a name="digital-signatures"></a>Assinaturas digitais

Os dados contidos em um formulário podem assinados digitalmente para ajudar a garantir que seu conteúdo não será alterado.
  
Para configurar um formulário para usar assinaturas digitais, selecione a opção **Permitir assinatura de todo o formulário** ou **Permitir assinatura de partes do formulário** na seção **Assinaturas digitais** da caixa de diálogo **Opções de formulário** disponível no Microsoft Office Backstage do designer de formulário do InfoPath. Ao preencherem o formulário, os usuários podem assinar e verificar formulários clicando no botão **Assinar formulário** na guia **Informações** do Microsoft Office Backstage. Quando o formulário for aberto novamente, o usuário será alertado se o conteúdo do formulário foi alterado. 
  
-  Assinaturas digitais podem ser habilitadas para todo o formulário ou para conjuntos de dados específicos no formulário que podem ser assinados separadamente. 
    
- Você pode assinar apenas seções específicas de um formulário em vez de o formulário inteiro.
    
- Você pode especificar se deseja permitir um só assinatura ou múltiplas assinaturas. Você também pode especificar qual é a relação entre cada conjunto de dados que pode ser assinados. Por exemplo, você pode especificar se as assinaturas são coassinaturas paralelas ou se cada nova assinatura referenda todas as anteriores.
    
- Você pode usar o modelo de objeto do InfoPath para adicionar programaticamente informações personalizadas para o bloco de assinatura em um formulário totalmente confiável.
    
- Você pode melhorar a segurança das assinaturas digitais capturando e incluindo informações adicionais, como um carimbo de data/hora, como evidência de não repúdio. Como evidências adicionais fazem parte da assinatura, elas não poderão ser removidas sem invalidar a assinatura. Você pode a qualquer momento revogar ou examinar os dados capturados clicando em uma assinatura digital no formulário ou selecionando a assinatura digital da lista de assinaturas digitais exibida na caixa de diálogo **Assinaturas digitais**. 
    
-  Você pode inserir e visualizar uma assinatura no documento, bem como visualizar o formulário da maneira como ele foi apresentado a cada signatário. 
    
- A assinatura digital inclui também um instantâneo da visualização da maneira como ela foi apresentada ao signatário quando o formulário foi assinado. O instantâneo é armazenado como uma imagem codificada em base64 no formato de arquivo padrão PNG. 
    
## <a name="email-deployment"></a>Envio por email

Você pode enviar seus modelos de formulário como anexo de mensagem de email e movê-los de um local para outro. O envio por email é uma maneira fácil e eficaz de distribuir formulários para uso entre escritórios e de enviar formulários para usuários remotos.
  
É possível assinar digitalmente um modelo de formulário que você criou e, em seguida, configurar o nível de segurança para esse modelo de formulário como Confiança total. Além disso, quando são enviados como anexo de email, os formulários totalmente confiáveis assinados podem ser atualizados de maneira mais fácil e eficiente.
  
No designer do InfoPath, todos os formulários são criados com uma identidade. Essas informações ajudam o InfoPath a associar formulários a modelos de formulário no cache e a recuperar atualizações de formulários quando elas são postadas em um local compartilhado. Por padrão, o InfoPath cria duas identidades para modelos de formulário: uma ID de formulários e um Caminho de acesso (também chamado de atributo **publishURL**). Para mais informações sobre o envio por email, consulte o tópico [Níveis de segurança, envio por email e modelos de formulário remotos](security-levels-email-deployment-and-remote-form-templates.md).
  
## <a name="activex-controls"></a>Controles ActiveX

O InfoPath dá suporte à hospedagem de controles ActiveX em formulários abertos no editor do InfoPath. Os controles ActiveX podem ser preexistentes (com algumas restrições) ou podem ser escritos especificamente para o uso no InfoPath. Os controles ActiveX que são usados em formulários do InfoPath não são baixados automaticamente de sites da Web. Em vez disso, arquivos CAB e controles ActiveX que não estejam presentes no computador do usuário devem ser adicionados ao arquivo de modelo de formulário.
  
Quando um controle ActiveX é usado em um formulário e o controle não está registrado no computador do usuário, o comportamento quando o formulário é aberto depende das configurações do controle ActiveX no formulário. Não havendo um arquivo CAB no arquivo de modelo de formulário, o InfoPath não abrirá o formulário. Havendo um arquivo CAB no arquivo de modelo de formulário, o InfoPath iniciará o processo de instalação. Para que o InfoPath instale um arquivo CAB, o arquivo deverá estar assinado, e assinatura dever vir de um fornecedor confiável. Se o fornecedor ainda não estiver na lista de fornecedores confiáveis do usuário com um certificado presente (com uma cadeia de confiabilidade que leve a uma raiz de certificado confiável), o usuário precisará aceitar ou recusar confiar no fornecedor. Se o usuário optar por não confiar no fornecedor, o arquivo CAB para o controle não será instalado e o InfoPath não abrirá o formulário.
  
> [!NOTE]
> Controles ActiveX devem ser marcados como "Seguro para execução de script" e "Seguro para inicialização com dados não confiáveis" para serem usados no InfoPath. 
  
## <a name="net-security"></a>Segurança do .NET

Além de níveis de segurança específicos do InfoPath, modelos de formulário de código gerenciado também são compatíveis com recursos adicionais de segurança de acesso de código que se aplicam a códigos gerenciados executados em Common Language Runtime (CLR) do Microsoft .NET Framework.
  
Se o seu formulário for totalmente confiável, você poderá acessar automaticamente recursos fora o modelo de formulário. Qualquer assembly pode ser usado no código de lógica de negócios. Você pode personalizar o conjunto de permissões que é adicionado a um modelo de formulário de código gerenciado usando a ferramenta de política de segurança de acesso de código (Caspol.exe) ou a ferramenta de configuração do Microsoft .NET Framework. O InfoPath buscará um grupo de códigos predefinidos e aplicará o conjunto de permissões definido nesse grupo para o domínio do aplicativo (AppDomain) em que o código gerenciado é carregado e de onde ele é executado. As políticas de segurança personalizadas do .NET devem ser implantadas nos computadores cliente que executarão o modelo de formulário de código gerenciado.
  
Observe que a segurança do .NET concede o conjunto de permissões de Internet somente para códigos gerenciados executados em Sites confiáveis do Internet Explorer. Portanto, os formulários de código gerenciado do InfoPath não serão executados se forem publicados em um Site confiável.
  
## <a name="merging-forms"></a>Mesclar formulários

Você pode desativar o recurso de mesclagem de formulários para impedir que usuários importem dados de vários formulários para um único formulário.
  
Para habilitar ou desabilitar a mesclagem de formulários, use a caixa de seleção **Habilitar a mesclagem de formulários** na seção **Avançado** da caixa de diálogo **Opções de formulário**, disponível na guia **Informações** do Microsoft Office Backstage quando você cria o formulário. Quando a mesclagem de formulários está desabilitada, usuários não podem clicar em **Mesclar formulários** na guia **Compartilhar** do Microsoft Office Backstage ao preencherem um formulário. 
  
## <a name="submitting-forms"></a>Envio de formulários

Você pode desativar o recurso de envio de formulários para impedir que usuários enviem formulários.
  
Para habilitar ou desabilitar o envio de formulários, use a caixa de diálogo **Opções de envio**, disponível ao clicar em **Opções de envio** no menu da guia **Dados** no modo de criação. Quando o envio de formulários está desabilitado, usuários não podem clicar em **Enviar** na guia **Início** ao preencherem um formulário. 
  

