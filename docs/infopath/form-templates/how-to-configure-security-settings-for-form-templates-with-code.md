---
title: Definir configurações de segurança para modelos de formulário com código
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- implantação da diretiva de segurança empacotar as URLs de [infopath 2007], [InfoPath 2007], atribuindo FullTrust, código de segurança de acesso [InfoPath 2007], UNCs [InfoPath 2007], atribuindo FullTrust, CAS [InfoPath 2007], [InfoPath 2007] de segurança, configuração, [de grupos de código FullTrust do InfoPath 2007], [InfoPath 2007], atribuindo a UNCs, FullTrust [InfoPath 2007], atribuindo a URLs
localization_priority: Normal
ms.assetid: 24d1a322-581f-497e-b97b-bd02c4516551
description: Você pode personalizar o conjunto de permissões que é aplicado a um modelo de formulário de código gerenciado do InfoPath usando o snap-in de configuração do .NET.
ms.openlocfilehash: f04ce71875eac7695d2900131ca7c9cd333fa90f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765620"
---
# <a name="configure-security-settings-for-form-templates-with-code"></a>Definir configurações de segurança para modelos de formulário com código

Você pode personalizar o conjunto de permissões que é aplicado a um modelo de formulário de código gerenciado do InfoPath usando o snap-in de configuração do .NET.
  
O common language runtime (CLR) hospedado pelo InfoPath procurará um grupo de código predefinido chamado *Modelos de formulário do InfoPath* no nível de diretiva de máquina sob o grupo All_Code. O CLR aplicará os conjuntos de permissões que estão definidos de acordo com esse grupo para o domínio de aplicativo (AppDomain) onde o código do formulário é executado. Isso permite que você personalize os conjuntos de permissões são concedidos aos modelos de formulário de código gerenciado do InfoPath. Por exemplo, você pode conceder a um modelo de formulário baixado de http://MySite permissão para acessar o Active Directory. 
  
Para a diretiva de segurança personalizadas definida usando o snap-in de configuração do .NET a ser aplicado, ele deve ser implantado em todos os computadores cliente onde o modelo de formulário será executado.
  
Para obter mais informações sobre o modelo de segurança para o InfoPath gerenciado modelos de formulário de código, consulte [Sobre o modelo de segurança para modelos de formulário com código](about-the-security-model-for-form-templates-with-code.md)
  
## <a name="creating-a-code-group-for-infopath-form-templates"></a>Criando um grupo de códigos para modelos de formulário do InfoPath

O procedimento a seguir criará um grupo de código que concede nenhuma permissão ao InfoPath gerenciado código modelos de formulário (exceto aqueles que são instalados ou registrados no computador local) em que você pode atribuir permissão define como modelos de formulário do InfoPath localizados em URLs ou UNCs específico. Para obter informações sobre como criar e atribuir permissão define a grupos de código dentro do `InfoPath Form Templates` código grupo, consulte o procedimento a seguir. 
  
> [!NOTE]
> Diferentemente da ferramenta de **configuração do Microsoft .NET Framework 1.1** é instalada com o pacote redistribuível do Microsoft .NET Framework 1.1, a **configuração do Microsoft .NET Framework 2.0** é instalado apenas com o Microsoft .NET Framework 2.0 software Development Kit (SDK). 
  
### <a name="to-create-a-custom-security-code-group-for-infopath-managed-code-forms"></a>Para criar um grupo de códigos de segurança personalizada para o InfoPath gerenciados formulários de código

1. No menu **Iniciar** , aponte para **Ferramentas administrativas**e clique em **configuração do Microsoft .NET Framework 2.0**.
    
    Se você não tiver **Ferramentas administrativas** no menu **Iniciar** , no **Painel de controle** de abrir **Ferramentas administrativas**e, em seguida, clique duas vezes em **configuração do Microsoft .NET Framework 2.0**.
    
2. Em **Meu computador**, expanda o nó de **Diretiva de segurança de tempo de execução** , o nó de **máquina** , o nó de **Grupos de código** , o nó **All_Code** e com o botão direito no nó **All_Code** e clique em **novo** para abrir o **Create Grupo de códigos** caixa de diálogo. 
    
3. Nomeie o novo grupo de código `InfoPath Form Templates` (este texto deve ser exato) e, em seguida, clique em **Avançar**.
    
4. Definir o tipo de condição para o grupo de código para **Todo o código**e, em seguida, clique em **Avançar**.
    
5. Clique em **Definir permissão de uso existente**, atribua o conjunto de permissões **Nothing** ao grupo código, clique em **Avançar**e, em seguida, clique em **Concluir**.
    
6. Para aplicar as novas configurações, feche e reinicie o InfoPath.
    
Se você preferir, você pode gerenciar a permissão definida para todos os modelos de formulário de código gerenciado do InfoPath, atribuindo-se um conjunto de permissões que não seja **Nothing** conjunto de permissões para o grupo de códigos de **Modelos de formulário do InfoPath** . 
> [!NOTE]
> Você pode alterar a permissão definida para um grupo de segurança de códigos a qualquer momento clicando com o grupo a. **NET Configuration 2.0** snap-in, clicando em **Propriedades**e, em seguida, clicando na guia **Permission Set** . 
  
## <a name="assigning-fulltrust-to-forms-at-a-specific-url-or-unc"></a>Atribuindo FullTrust aos formulários em um UNC ou URL específica

Você pode criar grupos de código sob o grupo de **Modelos de formulário do InfoPath** para conceder a permissão de confiança total definida como modelos de formulário de uma localidade específica de URL ou UNC. Depois de fazer isso, cada modelo de formulário publicado no local especificado será executado totalmente confiável. 
  
> [!NOTE]
> Um modelo de formulário é carregado a partir do computador local (grupo de código de zona do meu computador) seja carregado pelo InfoPath usando uma URL aleatória. Por esse motivo, você não pode usar o procedimento a seguir para conceder a permissão FullTrust definida como tal um modelo de formulário. Para conceder a permissão FullTrust de um modelo de formulário instalado localmente definida, use um dos procedimentos descritos na seção "Implantando o formulário modelos que exigem confiança total" do tópico [Implantar modelos de formulário do InfoPath com código](how-to-deploy-infopath-form-templates-with-code.md) . 
  
### <a name="to-assign-fulltrust-to-infopath-forms-at-a-specific-url-or-unc-location"></a>Para atribuir FullTrust para formulários do InfoPath em um local específico de URL ou UNC

1. No menu **Iniciar** , aponte para **Ferramentas administrativas**e clique em **configuração do Microsoft .NET Framework 2.0**.
    
    Se você não tiver **Ferramentas administrativas** no menu **Iniciar** , no **Painel de controle** de abrir **Ferramentas administrativas**e, em seguida, clique duas vezes em **configuração do Microsoft .NET Framework 2.0**.
    
2. Em **Meu computador**, expanda o nó de **Diretiva de segurança de tempo de execução** , o nó de **máquina** , o nó de **Grupos de código** , o nó **All_Code** e, em seguida, clique no nó de **Modelos de formulário do InfoPath** . 
    
3. Na lista de **tarefas** no painel direito, clique em **Adicionar um grupo de códigos filho**, o nome do grupo de código e clique em **Avançar**.
    
4. Na lista **Escolher o tipo de condição para este grupo de código** , selecione a **URL**e, em seguida, insira a URL ou UNC para a localização dos modelos de formulário de código gerenciado do InfoPath que você deseja conceder **a permissão FullTrust** . 
    
    Para restringir a permissão definida como um modelo de formulário simples, especifique o caminho completo do modelo de formulário específico. Por exemplo:
    
     `\\MyServer\MyShare\MyFormTemplate.xsn`
    
     `http://MySite/MySubsite/MyFormTempate.xsn`
    
    Para conceder a permissão definida como todos os modelos de formulário em uma URL ou UNC, omita o nome do modelo e adicione um asterisco no final da URL ou UNC. Por exemplo:
    
     `\\MyServer\MyShare\*`
    
     `http://MySite/MySubsite/*`
    
5. Clique em **Avançar**, **conjunto de permissões de uso existente** e clique atribua a permissão **FullTrust** definida como código de grupo. 
    
6. Clique em **Avançar**e, em seguida, clique em **Concluir**.
    
7. Para aplicar as novas configurações, feche e reinicie o InfoPath.
    
> [!NOTE]
> Para aplicar um conjunto de permissões mais restritivas ou personalizado, selecione a opção apropriada em vez de **FullTrust** na etapa 4. 
  
## <a name="creating-a-deployment-package-for-infopath-security-policy"></a>Criando um pacote de implantação para a diretiva de segurança do InfoPath

Depois de definir a diretiva de segurança personalizada para modelos de formulário gerenciado do InfoPath, você pode criar um pacote do Windows Installer (. msi) para implantar essa diretiva de segurança nos computadores dos usuários usando a diretiva de grupo ou o Microsoft Systems Management Server.
  
### <a name="to-create-a-deployment-package-for-custom-infopath-security-policy"></a>Para criar um pacote de implantação para a diretiva de segurança personalizada do InfoPath

1. No menu **Iniciar** , aponte para **Ferramentas administrativas**e clique em **configuração do Microsoft .NET Framework 2.0**.
    
    Se você não tiver **Ferramentas administrativas** no menu **Iniciar** , no **Painel de controle** de abrir **Ferramentas administrativas**e, em seguida, clique duas vezes em **configuração do Microsoft .NET Framework 2.0**.
    
2. Com o botão direito **Em tempo de execução de diretiva de segurança**e, em seguida, clique em **Criar pacote de implantação**.
    
3. Em **Selecione a política de segurança para implantar**, clique em **automática**, especifique a pasta e o nome do arquivo de pacote do Windows Installer e, em seguida, clique em **Avançar**.
    
4. Clique em **Concluir** para criar o pacote de implantação. 
    
5. Para obter informações sobre como usar a ferramenta de configuração do .NET Framework, pesquise a Ajuda do Visual Studio ou o site do MSDN "Ferramenta .NET Framework Configuration (Mscorcfg. msc)".
    
## <a name="see-also"></a>Confira também



[Sobre o modelo de segurança para modelos de formulário com código](about-the-security-model-for-form-templates-with-code.md)

