---
title: Conceitos de segurança adicionais de formulários do InfoPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 77425a61-bf33-b3d8-442a-caee48e54a48
description: O modelo de segurança do Microsoft InfoPath baseia-se no modelo de segurança implementado pelo Internet Explorer. O modelo de segurança do Internet Explorer ajuda a proteger seu computador contra operações sem segurança usando zonas de segurança e níveis. Trabalhando em conjunto com o modelo de segurança do Internet Explorer, o InfoPath fornece para dois tipos de implantação de formulário que afetam o funcionamento de um formulário do InfoPath dentro desse modelo de segurança.
ms.openlocfilehash: dc155e2c2962e2cca2b4465e5a9632f92488cef9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765584"
---
# <a name="additional-infopath-form-security-concepts"></a>Conceitos de segurança adicionais de formulários do InfoPath

O modelo de segurança do Microsoft InfoPath baseia-se no modelo de segurança implementado pelo Internet Explorer. O modelo de segurança do Internet Explorer ajuda a proteger seu computador contra operações sem segurança usando zonas de segurança e níveis. Trabalhando em conjunto com o modelo de segurança do Internet Explorer, o InfoPath fornece para dois tipos de implantação de formulário que afetam o funcionamento de um formulário do InfoPath dentro desse modelo de segurança.
  
- **Formulários baseados em URL** Esse método de implantação é o padrão durante a publicação de um formulário do InfoPath para um servidor Web, uma biblioteca de formulários do SharePoint Foundation ou um compartilhamento de arquivo. Esses formulários são conhecidos como formulários baseados em URL porque um usuário normalmente abre o formulário da URL de onde o formulário é publicado e URL especificado no atributo **publishUrl** do elemento **xDocumentClass** no arquivo de definição de formulário (. xsf). Formulários baseados em URL são considerados em área restrita, porque eles tem acesso restrito a recursos do sistema e outras áreas potenciais de risco. Um formulário baseado em URL tem o mesmo nível de permissões, como uma página da Web que é aberto no mesmo local em que o arquivo de modelo de formulário (. xsn).
    
- **Formulários baseados em URN** Esse método de implantação é para formulários que requerem acesso aos recursos do sistema e outros recursos externos, como os controles ActiveX e outros componentes de software. Você pode implantar os formulários do InfoPath como formulários totalmente confiáveis. Tais formulários são também conhecido como formulários baseados em URN porque, em vez de especificar o atributo **publishUrl** , elas especificam um nome de recurso uniforme (URN) no atributo **name** do elemento **xDocumentClass** no arquivo de definição de formulário (. xsf). Esta classe do formulário pode solicitar confiança total, se o atributo **requireFullTrust** do elemento **xDocumentClass** estiver definido como `"yes"` no arquivo de definição de formulário (. xsf). Formulários baseados em URN devem ser registrados no computador cliente por um programa de instalação ou o script. Nesse caso, o formulário obtém as mesmas permissões que um aplicativo que está sendo executado no computador local. 
    
Em conjunto com esses dois métodos de implantação de formulário, cada método e a propriedade no modelo de objeto do InfoPath tem um título que controla a nível quando esse método ou a propriedade pode ser chamada a partir de script executado a partir do formulário.
  
## <a name="understanding-infopath-integration-with-the-internet-explorer-security-model"></a>Noções básicas sobre a integração do InfoPath com o modelo de segurança do Internet Explorer

Internet Explorer implementa zonas de segurança que permitem controlar o nível de acesso concedido ao computador por páginas da Web que você abre. O InfoPath usa algumas dessas zonas para determinar o nível de acesso que formulários são concedidos aos recursos no seu computador. Por padrão, os formulários do InfoPath são executados em um local de cache que tem acesso negado para recursos críticos do sistema. Formulários que são permitidos acesso total a recursos do sistema são chamados formulários totalmente confiáveis. Formulários totalmente confiáveis geralmente estão instalados e registrados usando um script ou um programa de instalação ou são assinados digitalmente para que eles podem receber um nível mais alto de permissões.
  
Os formulários do InfoPath em cache são identificados pela URL ou o URN especificada no arquivo de definição de formulário do formulário (. xsf). O tipo de identificação usada e o domínio (local) do qual o modelo de formulário for aberto determina quais permissões de zona de segurança do Internet Explorer herdarão o formulário. Formulários identificados por uma URL são armazenados em cache para o computador do usuário, que permite o uso offline do formulário. Esses formulários baseados em URL herdam suas permissões de segurança e de seus direitos de acesso específicos, como acesso entre domínios, as configurações de segurança do Internet Explorer aplicáveis ao local original do modelo de formulário. Modelos de formulário armazenados em um servidor Web ou um servidor executando o SharePoint Foundation executado em Internet ou zona da intranet Local, dependendo do domínio do servidor. Formulários instalados identificados por um URN, por outro lado, herdam suas permissões a zona de computador Local, que concede um nível de permissões similares de arquivos de aplicativo HTML (. HTA).
  
Formulários totalmente confiáveis são identificados por seu URN e se o atributo **requireFullTrust** do elemento **xDocumentClass** no arquivo de definição (. xsf) do formulário é definido como `"yes"`. No InfoPath, depois formulários totalmente confiáveis são instalados, eles aparecem na guia **New** no editor do Microsoft Office Backstage do InfoPath. 
  
Para uma discussão detalhada de como formulários totalmente confiáveis funcionam e como criar e implantá-las, consulte [Understanding totalmente confiáveis formulários](understanding-fully-trusted-forms.md).
  
## <a name="trusting-installed-forms"></a>Confiando em formulários instalados

A capacidade de usar formulários confiáveis pode ser habilitada ou desabilitada em computadores individuais. Quando um computador é configurado para confiar em formulários instalados, os usuários podem preencher formulários que requerem acesso aos recursos do seu computador.
  
No editor do InfoPath, você configurar um computador para confiar formulários instalados no Backstage clicando em **Opções**, **Central de confiabilidade**, **Configurações da Central de confiabilidade**e em seguida, selecionando a verificação de **Permitir que formulários completamente confiáveis sejam executados no meu computador** caixa na guia **Editores confiáveis** da caixa de diálogo **Central de confiabilidade** . 
  
## <a name="using-security-features-in-infopath"></a>Usar os recursos de segurança do InfoPath

O modelo de segurança do InfoPath ajuda a proteger os usuários contra as seguintes ameaças trazidas por modelos de modo mal-intencionado criados:
  
- O potencial de divulgação de informações confidenciais do seu computador local ou fontes de dados remotos.
    
- O uso mal-intencionado de controles ActiveX.
    
- O uso mal-intencionado de propriedades e métodos do modelo de objeto do InfoPath.
    
## <a name="cross-domain-data-access"></a>Acesso a dados entre domínios

Cenários de riscos de segurança é conhecida como acesso a dados entre domínios.
  
O modelo de segurança do Internet Explorer InfoPath é construído fornece uma configuração denominada **acessar fontes de dados entre domínios**. Por padrão, essa configuração desabilita o acesso entre domínios para formulários do InfoPath que residem nas zonas de segurança de sites da Internet e restrito. Solicita ao usuário para permitir ou não o acesso entre domínios para formulários do InfoPath que residem na zona de segurança intranet Local, e ela permite o acesso entre domínios para formulários do InfoPath que residem nas zonas de **sites confiáveis** ou **Máquina Local** . 
  
## <a name="use-of-the-infopath-html-task-pane"></a>Uso do painel de tarefas de HTML do InfoPath

O painel de tarefas do InfoPath HTML permite a renderização de páginas da Web, como arquivos. htm,. asp e. hta. As páginas referenciadas de painéis de tarefas podem ser localizadas dentro ou fora do modelo de formulário. A única restrição nas quais podem ser referenciados de fora o modelo de formulário é que a página da Web deve estar no mesmo domínio que o modelo de formulário, ou a zona de segurança no qual reside o modelo deve permitir que as permissões de acesso entre domínios para carregar o painel de tarefas.
  
O painel de tarefas não expõe uma barra de endereços ou a barra de status e, portanto, o usuário não tem como confirmando o local da fonte para o painel de tarefas ou se esse local está sendo acessado por um canal criptografado (https). Por esse motivo, evite usar o painel de tarefas para exibir ou digitar informações confidenciais. O painel de tarefas foi projetado para exibir informações de ajuda dinâmica e controles de navegação entre modos de exibição e outros elementos de uma solução integrada. Além disso, a lógica de negócios e script no painel de tarefas de um modelo de formulário podem interagir uns com os outros. No entanto, essa interação é permitida somente se o modelo de formulário e o painel de tarefas estão no mesmo domínio, que ajuda a impedir que informações sejam trocadas entre domínios.
  
## <a name="cross-domain-data-access-prompts"></a>Solicita acesso a dados entre domínios

Se um modelo de formulário que requer acesso a dados entre domínios está localizado em uma zona de segurança que é definida para a solicitação de acesso a dados entre domínios (configuração padrão para a zona da intranet Local) e, em seguida, o usuário será solicitado se deseja permitir acesso. A opção do usuário, em seguida, persistirá para o restante da hora em que o formulário é aberto. Se você deve implantar os modelos de formulário do InfoPath que exigem acesso a dados entre domínios, você deve implantar esses modelos de formulários totalmente confiáveis ou torná-los disponíveis em um servidor que está na zona de segurança de sites confiáveis, para evitar solicitando que os usuários para permitir o acesso. Os usuários não devem ser instruídos diminuir o nível de segurança de zona da intranet Local, para evitar esses avisos.
  
## <a name="forms-without-a-publishurl-attribute"></a>Formulários sem um atributo publishURL

Se o InfoPath carrega um modelo de formulário a partir do computador local e tem um atributo de em branco **publishUrl** ou o atributo está ausente, o formulário será colocado em uma zona de segurança mais restritiva. Isso é feito para reduzir as ameaças de um modelo de formulário mal-intencionado sendo distribuído por email. Como resultado, se o usuário salvar esse modelo de formulário no disco, será possível executar com as permissões de um formulário que reside na zona da **Máquina Local** . 
  
## <a name="unsafe-activex-controls"></a>Controles ActiveX não segura

O cenário mais comum do uso mal-intencionado de controles ActiveX pode ocorrer se um autor usa o script com um controle ActiveX que fornece métodos para acessar o sistema de arquivos para recuperar arquivos pessoais e listas de senhas, excluir arquivos ou desabilitar o usuário sistema. Um formulário do InfoPath pode usar controles ActiveX apenas a partir de script no arquivo de script principal de um formulário (script. js) ou scripts em um painel de tarefas. InfoPath não permite script nos modos de exibição do InfoPath executem controles ActiveX.
  
O modelo de segurança do Internet Explorer Microsoft InfoPath é construído fornece que uma configuração chamada **inicializar e executar scripts de controles ActiveX não marcados como não seguros** que, por padrão, resulte nas seguintes ações para formulários do InfoPath ou painéis de tarefa que tentam para inicializar e criar script de controles ActiveX que são marcados como não seguros para script. 
  
|**Zona de segurança/implantação**|**Action**|
|:-----|:-----|
|Internet  <br/> |Desabilitado  <br/> |
|Intranet local  <br/> |Desabilitado  <br/> |
|Sites restritos  <br/> |Desabilitado  <br/> |
|Sites confiáveis  <br/> |Prompt  <br/> |
|Meu computador  <br/> |Prompt  <br/> |
|Formulário totalmente confiável  <br/> |Habilitar  <br/> |
   
## <a name="malicious-use-of-the-infopath-object-model"></a>Uso mal-intencionado do modelo de objeto do InfoPath

Da mesma forma como os controles ActiveX chamados de script, os métodos do InfoPath e as propriedades chamadas do código podem representar diferentes níveis de risco. Por exemplo, o método [SaveAs(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx) da classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) pode ser usado para gravar dados em qualquer lugar no sistema de arquivos. 
  
Para ajudar a proteger contra uso mal-intencionado dos membros do modelo de objeto do InfoPath, o modelo de objeto do InfoPath implementa três níveis de segurança que determinam como e onde um membro de modelo de objeto específico pode ser usado. Existem três níveis de segurança no modelo de objeto do InfoPath:
  
- **0** membros de modelo de objeto que podem ser acessados sem restrições. Esses membros do modelo de objeto são seguros e, portanto, podem ser acessados sem restrições. 
    
- **2** permissões de acesso de membros do modelo de objeto que podem ser acessados apenas por formulários sendo executados no mesmo domínio que o formulário atualmente aberto, ou por formulários que tiverem sido concedidos a dados entre domínios. Modelos de formulário restrito que chamam os métodos do modelo de objeto de nível 2 de segurança terá êxito somente se eles estão acessando os recursos contidos no modelo de formulário em si. 
    
- **3** membros de modelo de objeto que podem ser acessados apenas por formulários totalmente confiáveis. 
    
- Cada um dos tópicos para as propriedades e métodos na referência de modelo de objeto do InfoPath contém uma seção de segurança que especifica o nível de segurança que se aplica a esse membro de modelo de objeto.
    
- Segurança de nível **1** está reservado para uso futuro. 
    
## <a name="summary"></a>Resumo

A tabela a seguir resume as permissões padrão para cada método de implantação de formulário do InfoPath. Permissões se baseiam em zona de segurança para o domínio do qual se origina o modelo de formulário.
  
|**Zona de segurança**|**Implantação**|**Permissões padrão**|
|:-----|:-----|:-----|
||**Baseado em URL** <br/> |**Baseado em URN** <br/> |**ActiveX marcado não seguro para scripts** <br/> |**Acesso a dados entre domínios** <br/> |**Nível de segurança do modelo de objeto** <br/> |
|Sites restritos  <br/> |N/A  <br/> |N/A  <br/> |N/A  <br/> |N/A  <br/> |N/A  <br/> |
|Internet  <br/> |X  <br/> ||Desativar  <br/> |Desativar  <br/> |2  <br/> |
|Intranet local  <br/> |X  <br/> ||Desativar  <br/> |Prompt  <br/> |2  <br/> |
|Sites confiáveis  <br/> |X  <br/> ||Prompt  <br/> |Habilitar  <br/> |2  <br/> |
|Máquina local  <br/> |X  <br/> |X  <br/> |Desativar  <br/> |Prompt  <br/> |2  <br/> |
|Formulário totalmente confiável  <br/> |X (assinado por um editor confiável)  <br/> |X  <br/> |Habilitar  <br/> |Habilitar  <br/> |3  <br/> |
|Formulário totalmente confiável  <br/> ||X  <br/> |Habilitar  <br/> |Habilitar  <br/> |3  <br/> |
|Restricted  <br/> ||X  <br/> |Nenhum ActiveX (exceto uma lista limitada codificadas)  <br/> |Desativar  <br/> |2  <br/> |
|Restricted  <br/> |X  <br/> ||Nenhum ActiveX (exceto uma lista limitada codificadas)  <br/> |Desativar  <br/> |2  <br/> |
|Restricted  <br/> |X  <br/> |X  <br/> |Nenhum z ActiveX (exceto uma lista limitada codificadas)  <br/> |Desativar  <br/> |2  <br/> |
   
Para obter informações sobre segurança geral diretrizes ao desenvolver formulários, consulte [As diretrizes de segurança para o desenvolvimento de formulários do InfoPath](security-guidelines-for-developing-infopath-forms.md).
  
## <a name="understanding-other-security-features"></a>Noções básicas sobre outros recursos de segurança

O InfoPath fornece outras medidas de segurança para formulários que incluem a proteção de design do formulário usando assinaturas digitais, gerenciando determinadas operações de formulário, como mesclagem e envio e confiando em formulários instalados. As seções a seguir descrevem essas medidas de segurança do formulário e onde eles estão habilitados no InfoPath.
  
## <a name="digital-signatures"></a>Assinaturas digitais

Os dados contidos em um formulário podem ser assinados digitalmente para ajudar a garantir que o seu conteúdo não será alterado.
  
Configurar um formulário para usar assinaturas digitais, selecionando a opção **Permitir assinatura todo o formulário** ou **Permitir assinatura de partes do formulário** na seção de **Assinaturas digitais** da caixa de diálogo **Opções de formulário** , que está disponível em o Microsoft Office Backstage no designer de formulários do InfoPath. Durante o preenchimento do formulário, os usuários podem então entrar e verificar formulários clicando no botão de **Formulário de entrada** , na guia **informações** do Microsoft Office Backstage. Quando o formulário é aberto novamente, o usuário será alertado se o conteúdo do formulário tiver sido alterado. 
  
-  Assinaturas digitais podem ser habilitadas para o formulário inteiro ou para conjuntos de dados no formato que pode ser conectado separadamente específicos. 
    
- Você pode optar por assinar apenas as seções específicas de um formulário, em vez de todo o formulário.
    
- Você pode especificar se deseja permitir único ou vários assinaturas. Você também pode especificar o que é o relacionamento para cada conjunto de dados que podem ser assinados. Por exemplo, você pode especificar se as assinaturas são assinaturas de colegas paralelas ou se cada nova assinatura countersigns todas as anteriores.
    
- Você pode usar o modelo de objeto do InfoPath para adicionar informações personalizadas de maneira programática para o bloco de assinatura em um formulário totalmente confiável.
    
- Você pode melhorar a segurança de assinaturas digitais mediante a captação e incluindo informações adicionais, como um carimbo de hora, como evidência não repúdio. Como a evidência adicional é parte da assinatura, ele não pode ser removido sem invalidar a assinatura. É possível qualquer hora do cancelamento ou examinar os dados capturados clicando em uma assinatura digital no formulário ou selecionando uma assinatura digital da lista de assinaturas digitais exibido na caixa de diálogo **Assinaturas digitais** . 
    
-  Você pode inserir e ver uma assinatura do documento e exiba o formulário como ela foi apresentada para cada signatário. 
    
- A assinatura digital também inclui um instantâneo do modo de exibição foi apresentado para o signatário quando o formulário foi assinado. O instantâneo é armazenado como uma imagem codificado na base64 no formato de arquivo PNG padrão. 
    
## <a name="email-deployment"></a>Implantação de email

Você pode implantar seus modelos de formulário como um anexo em uma mensagem de email e mover os modelos de formulário de um local para outro. Implantação de email é uma maneira fácil e eficaz para distribuir formulários para uso interno e implantar os formulários para usuários remotos.
  
Você pode assinar digitalmente um modelo de formulário que você projetar e em seguida, defina o nível de segurança para esse modelo de formulário como confiança total. Além disso, os formulários totalmente confiáveis assinados, quando eles são implantados como um anexo de email, podem ser atualizados mais rapidez e eficiência.
  
Todos os formulários do InfoPath designer são criados com uma identidade. Essa informação ajuda InfoPath associar a modelos de formulário no cache de formulários e recuperar atualizações aos formulários quando são lançadas para um local compartilhado. Por padrão, o InfoPath cria duas identidades para modelos de formulário: uma identificação de formulário e um caminho de acesso (também conhecido como o atributo **publishURL** ). Você pode encontrar mais informações sobre a implantação de email no tópico [níveis de segurança, implantação de email e modelos de formulário remotos](security-levels-email-deployment-and-remote-form-templates.md).
  
## <a name="activex-controls"></a>Controles ActiveX

O InfoPath oferece suporte a hospedagem os controles ActiveX em formulários abertos no editor do InfoPath. Os controles ActiveX podem ser preexistente (com algumas restrições) ou podem ser escritos especificamente para uso com o InfoPath. Controles ActiveX que são usados em formulários do InfoPath não são baixados automaticamente de sites da Web. Em vez disso, os arquivos CAB para os controles ActiveX que ainda não estão presentes no computador do usuário devem ser adicionados ao arquivo de modelo de formulário.
  
Quando um controle ActiveX é usado em um formulário e o controle não está registrado no computador do usuário, o comportamento quando o formulário é aberto depende as configurações de controle ActiveX dentro do formulário. Se nenhum arquivo CAB é incluído no arquivo de modelo de formulário, o InfoPath não abrirá o formulário. Se o arquivo CAB estiver presente no arquivo de modelo de formulário, o InfoPath iniciará um processo de instalação. Para o InfoPath instalar um arquivo CAB, o arquivo deve ser assinado e a assinatura deve ser de um fornecedor confiável. Se o publisher não ainda estiver na lista de editores confiáveis do usuário que possui um certificado presente (com uma cadeia de confiança que leva a raiz de um certificado confiável), o usuário será solicitado para aceitar ou recusar confiando o publisher. Se o usuário optar por não confiar no Editor, o arquivo CAB para o controle não será instalado e InfoPath não abrirá o formulário.
  
> [!NOTE]
> Controles ActiveX devem ser marcados como "Seguro para script" e "Seguros para inicialização com dados não confiáveis" para que possam ser usados no InfoPath. 
  
## <a name="net-security"></a>Segurança do .NET

Além dos níveis de segurança específicos do InfoPath, modelos de formulário de código gerenciado também oferecer suporte a recursos de segurança de acesso de código adicionais que se aplicam ao código gerenciado em execução sob o CLR Common Language Runtime () do Microsoft .NET Framework.
  
Se o seu formulário for totalmente confiável, ele automaticamente pode acessar recursos fora do modelo de formulário. Qualquer assembly pode ser usada no código de lógica de negócios. Você pode personalizar o conjunto de permissões que é adicionado a um modelo de formulário de código gerenciado usando a ferramenta de configuração do Microsoft .NET Framework ou a ferramenta de política de segurança de acesso do código (Caspol.exe). InfoPath procurará um grupo predefinido de código e aplicará o conjunto de permissões que é definido em que o grupo do domínio de aplicativo (AppDomain) onde o código gerenciado é carregado e do qual ele é executado. Políticas de segurança personalizadas .NET devem ser implantadas para os computadores cliente onde o modelo de formulário de código gerenciado será executado.
  
Observe que a segurança do .NET concede a permissão de Internet definida apenas como código gerenciado executado em Sites confiáveis do Internet Explorer. Portanto, formulários de código gerenciado do InfoPath não serão executado se elas são publicadas em um Site confiável.
  
## <a name="merging-forms"></a>Mesclagem de formulários

Você pode desativar o recurso para impedir que usuários importando dados de vários formulários em um formulário simples de mesclagem de formulários.
  
Habilitar ou desabilitar a mesclagem usando a caixa de seleção **Habilitar mesclagem de formulários** , na seção **Avançado** da caixa de diálogo **Opções de formulário** , que está disponível da guia **informações** do Microsoft Office Backstage quando você cria o formulário de formulário . Quando a mesclagem de formulários está desabilitada, os usuários não podem clicar **Mesclar Formulários** na guia **compartilhamento** do Microsoft Office Backstage ao preencher um formulário. 
  
## <a name="submitting-forms"></a>Envio de formulários

Você pode desabilitar o recurso de envio do formulário para impedir que usuários enviar formulários.
  
Habilitar ou desabilitar o envio do formulário, usando a caixa de diálogo **Opções de envio** , que está disponível clicando em **Opções de envio** no menu de guia **dados** , no modo de design. Quando envio do formulário está desabilitado, os usuários não podem clique em **Enviar** na guia **início** ao preencher um formulário. 
  

