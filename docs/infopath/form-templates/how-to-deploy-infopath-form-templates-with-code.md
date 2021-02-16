---
title: Implantar modelos de formulário do InfoPath com código
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- implantação de modelos de formulário [infopath 2007],InfoPath 2007, implantação de modelos de formulário, modelos de formulário [InfoPath 2007], implantação, configurações de segurança do .NET Framework [InfoPath 2007],implantação [InfoPath 2007], modelos de formulário
localization_priority: Normal
ms.assetid: ab66e26d-74ee-4211-b387-1385183a6803
description: O código de formulário para um modelo de formulário de código gerenciado do InfoPath é compilado como um assembly executado no CLR (Common Language Runtime). This means that whenever you need to make changes to the form code, you must open its project in Visual Studio 2012, make changes in the code editor, recompile your form template, and then re-deploy the form template. Além disso, como o assembly particular de um modelo de formulário de código gerenciado está sendo executado em um domínio de aplicativo CLR hospedado, as configurações de segurança para formulários que exigem confiança total diferem um pouco dos modelos de formulário que não exigem confiança total.
ms.openlocfilehash: ba3629e786a224ea950e78bbec9a9fe94d4499de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406896"
---
# <a name="deploy-infopath-form-templates-with-code"></a>Implantar modelos de formulário do InfoPath com código

O código de formulário para um modelo de formulário de código gerenciado do InfoPath é compilado como um assembly executado no CLR (Common Language Runtime). This means that whenever you need to make changes to the form code, you must open its project in Visual Studio 2012, make changes in the code editor, recompile your form template, and then re-deploy the form template. Além disso, como o assembly particular de um modelo de formulário de código gerenciado está sendo executado em um domínio de aplicativo CLR hospedado, as configurações de segurança para formulários que exigem confiança total diferem um pouco dos modelos de formulário que não exigem confiança total.
  
## <a name="deploying-form-templates-that-do-not-require-full-trust"></a>Implantando modelos de formulário que não exigem confiança total

Se o código do formulário para seu modelo de formulário não usar membros do modelo de objeto do InfoPath que exigem confiança total e o modelo de formulário não usar recursos que exigem confiança total, você poderá publicar seu modelo de formulário diretamente do InfoPath usando o procedimento a seguir. Para obter informações sobre o modelo de segurança do InfoPath, consulte [Sobre o modelo de segurança para modelos de formulário com código.](about-the-security-model-for-form-templates-with-code.md)
  
### <a name="deploy-a-form-template-that-does-not-require-full-trust"></a>Implantar um modelo de formulário que não exige confiança total

1. Crie e depure seu modelo de formulário no Visual Studio 2012.
    
2. If you are working in the Visual Studio 2012 code editor, switch to InfoPath, click the **File** tab, and then click the button for the desired publishing location on the **Publish** tab. (If you have published the form template previously, you can click the **File** tab, and then click **Quick Publish** to republish the form template to the same location.) 
    
    O modelo de formulário é compilado e o **Assistente de Publicação** é lançado. Siga as etapas no Assistente **de Publicação** para implantar seu formulário no local de sua escolha. Para obter mais informações sobre como usar o **Assistente de** Publicação, pesquise na Ajuda do InfoPath por "Publicar um modelo de formulário".
    
## <a name="deploying-form-templates-that-require-full-trust"></a>Implantando modelos de formulário que exigem confiança total

Se o código do formulário para seu modelo de formulário usar membros do modelo de objeto do InfoPath que exigem confiança total ou o modelo de formulário usar recursos que exigem confiança total, você deverá assinar digitalmente seu arquivo de modelo de formulário (.xsn) com um certificado de assinatura de código de um editor confiável, no qual seus usuários serão solicitados a confiar quando abrirem o formulário. Isso também fará com que seu formulário seja totalmente confiável e, por sua vez, conceda o conjunto de permissões FullTrust ao código do formulário.
  
### <a name="compile-publish-and-digitally-sign-a-form-template"></a>Compilar, publicar e assinar digitalmente um modelo de formulário

1. Crie e depure seu modelo de formulário no Visual Studio 2012.
    
2. Se você estiver trabalhando no editor de código do Visual Studio 2012, alternar para o InfoPath, clique na guia Arquivo e em Opções **de Formulário.** 
    
3. Clique na **categoria Segurança e** Confiança. 
    
4. Em **Nível de Segurança,** des marque a caixa de seleção Determinar **automaticamente** o nível de segurança e selecione **Confiança Total.**
    
5. Em **Assinatura de Modelo de** Formulário , selecione **Assinar** este modelo de formulário, clique em Selecionar Certificado e especifique o certificado de assinatura de código com o qual assinar o modelo de formulário.
    
6. Clique **em OK** duas vezes para fechar a caixa de diálogo **Opções** de Formulário e salve suas alterações. 
    
7. Clique na **guia** Publicar e clique no botão para o local de publicação desejado. 
    
8. O modelo de formulário é compilado e o **Assistente de Publicação** é lançado. Siga as etapas no Assistente **de Publicação para** implantar seu modelo de formulário. Para obter mais  informações sobre como usar o Assistente de Publicação para implantar um modelo de formulário que exija confiança total, pesquise a Ajuda do InfoPath para "Publicar um modelo de formulário com confiança total". 
    
 **Anotações**
- Para assinar digitalmente um formulário, você deve ter um certificado de assinatura de código autenticado instalado em seu computador. Para adquirir esse certificado, entre em contato com uma autoridade de certificação ou com seu administrador de rede.
    
- Se você precisar fazer alterações no formulário após a publicação, deverá repetir o procedimento e assinar o modelo de formulário outra vez. Isso porque a alteração do formulário invalida a assinatura digital. Durante o desenvolvimento de um formulário que exija permissões de confiança total, você pode usar o procedimento descrito em Modelos de Formulário de Visualização e [Depuração](how-to-preview-and-debug-form-templates-that-require-full-trust.md) que exigem Confiança Total para registrar o modelo de formulário no computador local. 
    
## <a name="configuring-net-framework-security-settings"></a>Definindo as configurações de segurança do .NET Framework

Para obter controle adicional sobre as permissões concedidas ao código gerenciado em execução em um modelo de formulário de código gerenciado do InfoPath, você pode usar o utilitário de configuração do .NET Framework 2.0 para conceder um conjunto de permissões específico ao seu código de formulário.
  
> [!IMPORTANT]
> Definir as configurações de segurança do .NET Framework para um modelo de formulário de código gerenciado do InfoPath não afeta se os membros do modelo de objeto do InfoPath que exigem confiança total podem ser executados. Você deve assinar digitalmente ou registrar um modelo de formulário conforme descrito anteriormente neste tópico para habilitar chamadas para membros do modelo de objeto do InfoPath que exigem confiança total. As configurações de segurança do .NET Framework se aplicam somente a chamadas para membros de classes do .NET Framework e componentes gerenciados que não sejam o modelo de objeto do InfoPath. 
  
### <a name="compile-publish-and-configure-net-security-settings-for-a-form-template"></a>Compilar, publicar e definir configurações de segurança do .NET para um modelo de formulário

1. Crie e depure seu modelo de formulário no Visual Studio 2012.
    
2. Se você estiver trabalhando no editor de código do Visual Studio 2012, alternar para o InfoPath, clique na guia Arquivo, clique em Publicar e clique no botão para o local de publicação desejado.  
    
    O modelo de formulário é compilado e o **Assistente de Publicação** é lançado. Siga as etapas no Assistente **de Publicação para** implantar seu modelo de formulário. Para obter mais informações sobre como usar o **Assistente de** Publicação, pesquise na Ajuda do InfoPath por "Publicar um modelo de formulário".
    
3. Execute o procedimento descrito na seção "Atribuindo FullTrust a Formulários em uma URL específica ou UNC" da seção Definir configurações de segurança para modelos de formulário [com código](how-to-configure-security-settings-for-form-templates-with-code.md)
    
## <a name="see-also"></a>Confira também

#### <a name="tasks"></a>Tarefas

[Definir configurações de segurança para modelos de formulário com código](how-to-configure-security-settings-for-form-templates-with-code.md)


[Sobre o modelo de segurança para modelos de formulário com código](about-the-security-model-for-form-templates-with-code.md)
  
[Visualizar e depurar modelos de formulário que exigem confiança total](how-to-preview-and-debug-form-templates-that-require-full-trust.md)

