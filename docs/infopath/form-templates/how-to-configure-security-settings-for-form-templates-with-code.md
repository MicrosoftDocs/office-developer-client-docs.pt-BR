---
title: Definir configurações de segurança para modelos de formulário com código
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- pacote de implantação de políticas de segurança [infopath 2007], URLs [InfoPath 2007], atribuição de FullTrust, segurança de acesso ao código [InfoPath 2007], UNCs [InfoPath 2007], atribuição de FullTrust, CAS [InfoPath 2007], segurança [InfoPath 2007], configuração, grupos de código [InfoPath 2007], FullTrust [InfoPath 2007], atribuição a UNCs, FullTrust [InfoPath 2007], atribuição a URLs
localization_priority: Normal
ms.assetid: 24d1a322-581f-497e-b97b-bd02c4516551
description: Você pode personalizar o conjunto de permissões aplicado a um modelo de formulário de código gerenciado do InfoPath usando o snap-in de Configuração do .NET.
ms.openlocfilehash: 77f3546d976bb5ea353aa3fbe58ba7af6cd92a6d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391413"
---
# <a name="configure-security-settings-for-form-templates-with-code"></a>Definir configurações de segurança para modelos de formulário com código

Você pode personalizar o conjunto de permissões aplicado a um modelo de formulário de código gerenciado do InfoPath usando o snap-in de Configuração do .NET.
  
A CLR (Common Language Runtime) hospedada pelo InfoPath procurará um grupo de códigos predefinido denominado *Modelos de Formulários do InfoPath* no nível da política de Máquina sob o grupo All_Code. A CLR aplicará os conjuntos de permissões definidos nesse grupo ao domínio do aplicativo (AppDomain) no qual o código de formulário é executado. Isso permite personalizar os conjuntos de permissões concedidos a modelos de formulário de código gerenciado do InfoPath. Por exemplo, você pode conceder a permissão para acessar o Active Directory a um modelo de formulário baixado de https://MySite. 
  
Para que a política de segurança personalizada definida usando o snap-in de Configuração do .NET seja aplicada, ela deve ser implantada em todos os computadores cliente em que o modelo de formulário será executado.
  
Para saber mais sobre o modelo de segurança para modelos de formulário de código gerenciado do InfoPath, consulte [Sobre o modelo de segurança para modelos de formulário com código](about-the-security-model-for-form-templates-with-code.md)
  
## <a name="creating-a-code-group-for-infopath-form-templates"></a>Criar um grupo de códigos para modelos de formulário do InfoPath

O procedimento a seguir criará um grupo de códigos que não concede permissões a modelos de formulário de código gerenciado do InfoPath (exceto aqueles instalados ou registrados no seu computador local) abaixo do qual você pode atribuir conjuntos de permissões a modelos de formulário do InfoPath localizados em URLs ou UNCs específicos. Para saber mais sobre como criar e atribuir conjuntos de permissões a grupos de códigos no grupo de códigos `InfoPath Form Templates`, consulte o procedimento a seguir. 
  
> [!NOTE]
> Ao contrário da ferramenta de **Configuração do Microsoft .NET Framework 1.1** instalada com o Pacote Redistribuível do Microsoft .NET Framework 1.1, a ferramenta de **Configuração do Microsoft .NET Framework 2.0** é instalada apenas com o Microsoft .NET Framework 2.0 Software Development Kit (SDK). 
  
### <a name="to-create-a-custom-security-code-group-for-infopath-managed-code-forms"></a>Para criar um grupo de códigos de segurança personalizados para formulários de código gerenciado do InfoPath

1. No menu **Iniciar**, aponte para **Ferramentas Administrativas** e clique em **Configuração do Microsoft .NET Framework 2.0**.
    
    Se você não tiver **Ferramentas Administrativas** no menu **Iniciar**, no **Painel de Controle**, abra **Ferramentas Administrativas** e clique duas vezes em **Configuração do Microsoft .NET Framework 2.0**.
    
2. Em **Meu Computador**, expanda o nó **Política de Segurança de Tempo de Execução**, nó **Máquina**, **Grupos de Código**, nó **All_Code** e clique com o botão direito no nó **All_Code** e clique em **Novo** para abrir a caixa de diálogo **Criar Grupo de Códigos**. 
    
3. Chame o novo grupo de códigos de `InfoPath Form Templates` (esse texto deve ser exato) e clique em **Avançar**.
    
4. Defina o tipo de condição para o grupo de códigos como **Todo o Código** e clique em **Avançar**.
    
5. Clique em **Usar conjunto de permissões existente**, atribua o conjunto de permissões **Nada** ao grupo de códigos, clique em **Avançar ** e depois em **Concluir**.
    
6. Para aplicar as novas configurações, feche e reinicie o InfoPath.
    
Se preferir, você pode gerenciar o conjunto de permissões para todos os modelos de formulário de código gerenciado do InfoPath, atribuindo um conjunto de permissões diferente de **Nada** ao grupo de códigos **Modelos de Formulário do InfoPath**. 
> [!NOTE]
> Você pode alterar o conjunto de permissões para um grupo de códigos de segurança a qualquer momento clicando com o botão direito do mouse no grupo no  snap-in **Configuração do .NET 2.0**, clicando em **Propriedades** e, em seguida, clicando na guia **Conjunto de Permissões**. 
  
## <a name="assigning-fulltrust-to-forms-at-a-specific-url-or-unc"></a>Atribuição de FullTrust a formulários em uma URL ou UNC específico

Você pode criar grupos de códigos no grupo **Modelos de Formulário do InfoPath** para conceder o conjunto de permissões de confiança total a modelos de formulário de uma determinada URL ou localização UNC. Depois de fazer isso, todos os modelos de formulário publicados na localização especificada serão totalmente confiáveis. 
  
> [!NOTE]
> Um modelo de formulário carregado do computador local (grupo de códigos da Zona Meu Computador) é carregado pelo InfoPath usando uma URL aleatória. Por esse motivo, você não pode usar o procedimento a seguir para conceder o conjunto de permissões FullTrust a esse modelo de formulário. Para conceder a um modelo de formulário instalado localmente o conjunto de permissões FullTrust, use um dos procedimentos descritos na seção "Implantação de modelos de formulário que exigem confiança total", no tópico [Implantar modelos de formulário do InfoPath com código](how-to-deploy-infopath-form-templates-with-code.md). 
  
### <a name="to-assign-fulltrust-to-infopath-forms-at-a-specific-url-or-unc-location"></a>Para atribuir FullTrust a formulários do InfoPath em uma URL ou localização UNC específica

1. No menu **Iniciar**, aponte para **Ferramentas Administrativas** e clique em **Configuração do Microsoft .NET Framework 2.0**.
    
    Se você não tiver **Ferramentas Administrativas** no menu **Iniciar**, no **Painel de Controle**, abra **Ferramentas Administrativas** e clique duas vezes em **Configuração do Microsoft .NET Framework 2.0**.
    
2. Em **Meu Computador**, expanda o nó **Política de Segurança de Tempo de Execução**, o nó **Máquina**, o nó **Grupos de Código**, o nó **All_Code** e clique no nó **Modelos de Formulário do InfoPath**. 
    
3. Na lista de **Tarefas** do painel direito, clique em **Adicionar um Grupo de Códigos Filho**, nomeie esse grupo de códigos e, em seguida, clique em **Avançar**.
    
4. Na lista **Escolha o tipo de condição para este grupo de códigos**, selecione **URL** e insira a URL ou o UNC para a localização dos modelos de formulário de código gerenciado do InfoPath aos quais você deseja conceder o conjunto de permissões **FullTrust**. 
    
    Para restringir o conjunto de permissões a um único modelo de formulário, especifique o caminho completo desse modelo de formulário específico. Por exemplo:
    
     `\\MyServer\MyShare\MyFormTemplate.xsn`
    
     `https://MySite/MySubsite/MyFormTempate.xsn`
    
    Para conceder o conjunto de permissões a todos os modelos de formulário em uma URL ou um UNC, omita o nome do modelo e adicione um asterisco ao final da URL ou do UNC. Por exemplo:
    
     `\\MyServer\MyShare\*`
    
     `https://MySite/MySubsite/*`
    
5. Clique em **Avançar** e, em seguida, clique em **Usar conjunto de permissões existente** e atribua o conjunto de permissões **FullTrust** ao grupo de códigos. 
    
6. Clique em **Avançar** e em **Concluir**.
    
7. Para aplicar as novas configurações, feche e reinicie o InfoPath.
    
> [!NOTE]
> Para aplicar um conjunto de permissões mais restritivo ou personalizado, selecione a opção apropriada em vez de **FullTrust** na etapa 4. 
  
## <a name="creating-a-deployment-package-for-infopath-security-policy"></a>Criação de um pacote de implantação para uma política de segurança do InfoPath

Depois de definir a política de segurança personalizada para modelos de formulário gerenciado do InfoPath, você pode criar um Pacote do Windows Installer (.msi) para implantar essa política de segurança nos computadores dos usuários, usando a Política de Grupo ou o Microsoft Systems Management Server.
  
### <a name="to-create-a-deployment-package-for-custom-infopath-security-policy"></a>Para criar um pacote de implantação para uma política de segurança personalizada do InfoPath

1. No menu **Iniciar**, aponte para **Ferramentas Administrativas** e clique em **Configuração do Microsoft .NET Framework 2.0**.
    
    Se você não tiver **Ferramentas Administrativas** no menu **Iniciar**, no **Painel de Controle**, abra **Ferramentas Administrativas** e clique duas vezes em **Configuração do Microsoft .NET Framework 2.0**.
    
2. Clique com o botão direito do mouse em **Política de Segurança de Tempo de Execução** e depois clique em **Criar Pacote de Implantação**.
    
3. Em **Selecione a política de segurança a ser implantada**, clique em **Máquina**, especifique a pasta e o nome do arquivo do Pacote do Windows Installer e clique em **Avançar**.
    
4. Clique em **Concluir** para criar o pacote de implantação. 
    
5. Para saber mais sobre como usar a ferramenta de Configuração do .NET Framework, procure "Ferramenta de Configuração do .NET Framework (Mscorcfg.msc)" na Ajuda do Visual Studio ou no site da MSDN.
    
## <a name="see-also"></a>Confira também



[Sobre o modelo de segurança para modelos de formulário com código](about-the-security-model-for-form-templates-with-code.md)

