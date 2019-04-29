---
title: Implantar modelos de formulário do InfoPath com código
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- implantar modelos de formulário [InfoPath 2007], InfoPath 2007, implantação de modelos de formulário, modelos de formulário [InfoPath 2007], implantação, configurações de segurança do .NET Framework [InfoPath 2007], implantação [InfoPath 2007], modelos de formulário
localization_priority: Normal
ms.assetid: ab66e26d-74ee-4211-b387-1385183a6803
description: O código de formulário para um modelo de formulário de código gerenciado do InfoPath é compilado como um assembly que é executado no Common Language Runtime (CLR). Isso significa que sempre que você precisar fazer alterações no código de formulário, será necessário abrir o projeto no Visual Studio 2012, fazer alterações no editor de código, recompilar o modelo de formulário e, em seguida, reimplantar o modelo de formulário. Além disso, como o assembly privado de um modelo de formulário de código gerenciado é executado em um domínio de aplicativo CLR hospedado, as configurações de segurança para formulários que exigem confiança total diferem de forma diferente de modelos de formulário que não exigem confiança total.
ms.openlocfilehash: ba3629e786a224ea950e78bbec9a9fe94d4499de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406896"
---
# <a name="deploy-infopath-form-templates-with-code"></a>Implantar modelos de formulário do InfoPath com código

O código de formulário para um modelo de formulário de código gerenciado do InfoPath é compilado como um assembly que é executado no Common Language Runtime (CLR). Isso significa que sempre que você precisar fazer alterações no código de formulário, será necessário abrir o projeto no Visual Studio 2012, fazer alterações no editor de código, recompilar o modelo de formulário e, em seguida, reimplantar o modelo de formulário. Além disso, como o assembly privado de um modelo de formulário de código gerenciado é executado em um domínio de aplicativo CLR hospedado, as configurações de segurança para formulários que exigem confiança total diferem de forma diferente de modelos de formulário que não exigem confiança total.
  
## <a name="deploying-form-templates-that-do-not-require-full-trust"></a>ImPlantando modelos de formulário que não exigem confiança total

Se o código de formulário do seu modelo de formulário não usar membros do modelo de objeto do InfoPath que exigem confiança total e o modelo de formulário não usar recursos que exijam confiança total, você poderá publicar o modelo de formulário diretamente do InfoPath usando o procedimento a seguir. Para obter informações sobre o modelo de segurança do InfoPath, consulte [sobre o modelo de segurança para modelos de formulário com código](about-the-security-model-for-form-templates-with-code.md).
  
### <a name="deploy-a-form-template-that-does-not-require-full-trust"></a>Implantar um modelo de formulário que não requer confiança total

1. Criar e depurar seu modelo de formulário no Visual Studio 2012.
    
2. Se você estiver trabalhando no editor de código do Visual Studio 2012, alterne para o InfoPath, clique na guia **arquivo** e, em seguida, clique no botão do local de publicação desejado na guia **publicar** . (se você já publicou o modelo de formulário, clique no menu Guia **arquivo** e clique em **publicação rápida** para republicar o modelo de formulário no mesmo local.) 
    
    O modelo de formulário é compilado e o **Assistente de publicação** é iniciado. Siga as etapas no **Assistente de publicação** para implantar seu formulário no local de sua escolha. Para obter mais informações sobre como usar o **Assistente de publicação**, pesquise "publicar um modelo de formulário" na ajuda do InfoPath.
    
## <a name="deploying-form-templates-that-require-full-trust"></a>ImPlantando modelos de formulário que exigem confiança total

Se o código de formulário do modelo de formulário usar membros do modelo de objeto do InfoPath que exigem confiança total ou se o modelo de formulário usar recursos que exijam confiança total, você deverá assinar digitalmente o arquivo de modelo de formulário (. xsn) com um certificado de assinatura de código de um confiável Publisher, que os usuários serão solicitados a confiar quando abrirem o formulário. Isso também fará com que seu formulário seja totalmente confiável e, por sua vez, conceda o conjunto de permissões FullTrust ao seu código de formulário.
  
### <a name="compile-publish-and-digitally-sign-a-form-template"></a>Compilar, publicar e assinar digitalmente um modelo de formulário

1. Criar e depurar seu modelo de formulário no Visual Studio 2012.
    
2. Se você estiver trabalhando no editor de código do Visual Studio 2012, alterne para o InfoPath, clique na guia **arquivo** e em **Opções de formulário**.
    
3. Clique na categoria **segurança e confiança** . 
    
4. Em **nível de segurança**, desmarque a caixa de seleção **determinar automaticamente o nível de segurança** e, em seguida, selecione **confiança total**.
    
5. Em **assinatura de modelo de formulário**, selecione **assinar este modelo de formulário**, clique em **Selecionar certificado**e especifique o certificado de assinatura de código com o qual assinar o modelo de formulário.
    
6. Clique em **OK** duas vezes para fechar a caixa de diálogo **Opções de formulário** e salve suas alterações. 
    
7. Clique na guia **publicar** e, em seguida, clique no botão do local de publicação desejado. 
    
8. O modelo de formulário é compilado e o **Assistente de publicação** é iniciado. Siga as etapas no **Assistente de publicação** para implantar o modelo de formulário. Para obter mais informações sobre como usar o **Assistente de publicação** para implantar um modelo de formulário que requer confiança total, pesquise a ajuda do InfoPath para "publicar um modelo de formulário com confiança total". 
    
 **Anotações**
- Para assinar digitalmente um formulário, você deve ter um certificado de assinatura de código autenticado instalado no seu computador. Para adquirir esse certificado, você deve entrar em contato com uma autoridade de certificação ou com seu administrador de rede.
    
- Se você precisar fazer alterações no formulário após a publicação, deverá repetir o procedimento e assinar novamente o modelo de formulário. Isso ocorre porque alterar o formulário invalida a assinatura digital. Durante o desenvolvimento de um formulário que requer permissões de confiança total, você pode usar o procedimento descrito em [Visualizar e depurar modelos de formulário que exigem confiança total](how-to-preview-and-debug-form-templates-that-require-full-trust.md) para registrar o modelo de formulário no computador local. 
    
## <a name="configuring-net-framework-security-settings"></a>Definindo configurações de segurança do .NET Framework

Para obter mais controle sobre as permissões concedidas ao código gerenciado em execução em um modelo de formulário de código gerenciado do InfoPath, você pode usar o utilitário de configuração do .NET Framework 2,0 para conceder um conjunto de permissões específico a seu código de formulário.
  
> [!IMPORTANT]
> A definição de configurações de segurança do .NET Framework para um modelo de formulário de código gerenciado do InfoPath não afeta se os membros do modelo de objeto do InfoPath que exigem confiança total podem ser executados. Você deve assinar digitalmente ou registrar um modelo de formulário, conforme descrito anteriormente neste tópico, para habilitar as chamadas para membros do modelo de objeto do InfoPath que exigem confiança total. A definição de configurações de segurança do .NET Framework aplica-se apenas às chamadas para membros de classes do .NET Framework e componentes gerenciados diferentes do modelo de objeto do InfoPath. 
  
### <a name="compile-publish-and-configure-net-security-settings-for-a-form-template"></a>Compilar, publicar e definir configurações de segurança do .NET para um modelo de formulário

1. Criar e depurar seu modelo de formulário no Visual Studio 2012.
    
2. Se você estiver trabalhando no editor de código do Visual Studio 2012, alterne para o InfoPath, clique na guia **arquivo** , em **publicar**e, em seguida, clique no botão do local de publicação desejado.
    
    O modelo de formulário é compilado e o **Assistente de publicação** é iniciado. Siga as etapas no **Assistente de publicação** para implantar o modelo de formulário. Para obter mais informações sobre como usar o **Assistente de publicação**, pesquise "publicar um modelo de formulário" na ajuda do InfoPath.
    
3. Execute o procedimento descrito na seção "atribuindo FullTrust a formulários em uma URL específica ou UNC" das [configurações de definição de segurança para modelos de formulário com código](how-to-configure-security-settings-for-form-templates-with-code.md)
    
## <a name="see-also"></a>Confira também

#### <a name="tasks"></a>Tarefas

[Definir configurações de segurança para modelos de formulário com código](how-to-configure-security-settings-for-form-templates-with-code.md)


[Sobre o modelo de segurança para modelos de formulário com código](about-the-security-model-for-form-templates-with-code.md)
  
[Visualizar e depurar modelos de formulário que exigem confiança total](how-to-preview-and-debug-form-templates-that-require-full-trust.md)

