---
title: Implantar modelos de formulário do InfoPath com código
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- implantando modelos de formulário [infopath 2007], InfoPath 2007, implantando modelos de formulário, implantar, configurações de segurança do .NET Framework [InfoPath 2007], [InfoPath 2007] de implantação, modelos de formulário de modelos de formulário [InfoPath 2007]
localization_priority: Normal
ms.assetid: ab66e26d-74ee-4211-b387-1385183a6803
description: O código do formulário para um modelo de formulário de código gerenciado do InfoPath é compilado como um assembly que é executado sob o common language runtime (CLR). Isso significa que sempre que você precisa fazer alterações no código de formulário, você deve abrir o seu projeto no Visual Studio 2012, fazer alterações no código editor, recompile seu modelo de formulário e então implantar novamente o modelo de formulário. Além disso, porque o assembly particular para um modelo de formulário de código gerenciado está sendo executado em um domínio de aplicativo hospedado CLR, as configurações de segurança para formulários que exigem confiança total diferem um pouco da modelos de formulário que não exigem confiança total.
ms.openlocfilehash: 56af865a80df75c7e1d973767066a03310cdde1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765604"
---
# <a name="deploy-infopath-form-templates-with-code"></a>Implantar modelos de formulário do InfoPath com código

O código do formulário para um modelo de formulário de código gerenciado do InfoPath é compilado como um assembly que é executado sob o common language runtime (CLR). Isso significa que sempre que você precisa fazer alterações no código de formulário, você deve abrir o seu projeto no Visual Studio 2012, fazer alterações no código editor, recompile seu modelo de formulário e então implantar novamente o modelo de formulário. Além disso, porque o assembly particular para um modelo de formulário de código gerenciado está sendo executado em um domínio de aplicativo hospedado CLR, as configurações de segurança para formulários que exigem confiança total diferem um pouco da modelos de formulário que não exigem confiança total.
  
## <a name="deploying-form-templates-that-do-not-require-full-trust"></a>Implantando modelos de formulário que não exigem confiança total

Se o código do formulário para o seu modelo de formulário não usa membros de modelo de objeto do InfoPath que exigem confiança total e o modelo de formulário não usa recursos que exigem confiança total, você pode publicar seu modelo de formulário diretamente do InfoPath usando o procedimento a seguir. Para obter informações sobre o modelo de segurança do InfoPath, consulte [Sobre o modelo de segurança para modelos de formulário com código](about-the-security-model-for-form-templates-with-code.md).
  
### <a name="deploy-a-form-template-that-does-not-require-full-trust"></a>Implantar um modelo de formulário que não exige confiança total

1. Criar e depurar seu modelo de formulário no Visual Studio 2012.
    
2. Se você estiver trabalhando no editor de código do Visual Studio 2012, alterne para o InfoPath, clique na guia **arquivo** e, em seguida, clique no botão para o local desejado de publicação na guia **Publicar** (se você tiver publicado o modelo de formulário anteriormente, você pode clicar o **Arquivo** guia e clique em **Publicar rápida** para republicar o modelo de formulário no mesmo local.) 
    
    O modelo de formulário é compilado e o **Assistente de publicação** é aberto. Siga as etapas no **Assistente de publicação** para implantar o formulário para o local de sua escolha. Para obter mais informações sobre como usar o **Assistente de publicação**, consulte a Ajuda do InfoPath para "Publicar um modelo de formulário".
    
## <a name="deploying-form-templates-that-require-full-trust"></a>Implantando modelos de formulário que exijam confiança total

Se o código do formulário para o seu modelo de formulário usa membros de modelo de objeto do InfoPath que exigem confiança total ou o modelo de formulário utiliza os recursos que exigem confiança total, você deve assinar digitalmente seu arquivo de modelo (. xsn) do formulário com um certificado confiável de assinatura de código fornecedor, seus usuários serão solicitados a confiar quando eles abrem o formulário. Isso também fazer com que o seu formulário totalmente confiáveis e, por sua vez conceder a permissão FullTrust definida como seu código de formulário.
  
### <a name="compile-publish-and-digitally-sign-a-form-template"></a>Compilar, publicar e assinar digitalmente um modelo de formulário

1. Criar e depurar seu modelo de formulário no Visual Studio 2012.
    
2. Se você estiver trabalhando no editor de código do Visual Studio 2012, alterne para o InfoPath, clique na guia **arquivo** e, em seguida, clique em **Opções de formulário**.
    
3. Clique na categoria de **segurança e confiança** . 
    
4. Em **Nível de segurança**, desmarque a caixa de seleção **determinar automaticamente o nível de segurança** e selecione **Confiança total**.
    
5. Em **Assinatura do modelo de formulário**, selecione **entrar esse modelo de formulário**, clique em **Selecionar certificado**e, em seguida, especifique o certificado com a qual assinar o modelo de formulário de assinatura de código.
    
6. Clique em **Okey** duas vezes para fechar a caixa de diálogo **Opções de formulário** e salve as alterações. 
    
7. Clique na guia **Publicar** e, em seguida, clique no botão para o local de publicação desejado. 
    
8. O modelo de formulário é compilado e o **Assistente de publicação** é aberto. Siga as etapas no **Assistente de publicação** para implantar seu modelo de formulário. Para obter mais informações sobre como usar o **Assistente de publicação** para implantar um modelo de formulário que requer confiança total, pesquise a Ajuda do InfoPath para "Publicar um modelo de formulário com confiança total". 
    
 **Notes**
- Para assinar digitalmente um formulário, você deve ter um instalado no computador de certificado de assinatura de código autenticado. Para adquirir desses certificados, você precisa contatar o administrador da rede ou uma autoridade de certificação.
    
- Se você precisar fazer alterações no formulário após a publicação, você deve repetir o procedimento e entrar novamente o modelo de formulário. Isso ocorre porque a alterar o formulário invalida a assinatura digital. Durante o desenvolvimento de um formulário que exige permissões de confiança total, você pode usar o procedimento descrito em [Visualizar e depurar modelos de formulário que exigem de confiança total](how-to-preview-and-debug-form-templates-that-require-full-trust.md) para registrar o modelo de formulário no computador local. 
    
## <a name="configuring-net-framework-security-settings"></a>Definindo configurações de segurança do .NET Framework

Para obter controle adicional sobre as permissões concedidas ao código gerenciado executado em um modelo de formulário de código gerenciado do InfoPath, você pode usar o utilitário de configuração do .NET Framework 2.0 para conceder uma permissão específica definida como seu código de formulário.
  
> [!IMPORTANT]
> Definindo configurações de segurança do .NET Framework para um InfoPath modelo de formulário de código gerenciado não afeta se membros de modelo de objeto do InfoPath que exigem confiança total podem ser executados. Digitalmente você deve entrar ou registrar um modelo de formulário, conforme descrito anteriormente neste tópico para habilitar chamadas aos membros de modelo de objeto do InfoPath que exigem confiança total. Configurando o .NET Framework configurações de segurança aplicam-se somente a chamadas para membros de classes do .NET Framework e componentes gerenciados que não seja o modelo de objeto do InfoPath. 
  
### <a name="compile-publish-and-configure-net-security-settings-for-a-form-template"></a>Compilar, publicar e definir configurações de segurança do .NET para um modelo de formulário

1. Criar e depurar seu modelo de formulário no Visual Studio 2012.
    
2. Se você estiver trabalhando no editor de código do Visual Studio 2012, alterne para o InfoPath, clique na guia **arquivo** , clique em **Publicar**e, em seguida, clique no botão para o local desejado de publicação.
    
    O modelo de formulário é compilado e o **Assistente de publicação** é aberto. Siga as etapas no **Assistente de publicação** para implantar seu modelo de formulário. Para obter mais informações sobre como usar o **Assistente de publicação**, consulte a Ajuda do InfoPath para "Publicar um modelo de formulário".
    
3. Execute o procedimento descrito na seção "Atribuindo FullTrust para formulários em um específicos URL ou UNC" [Configurar as definições de segurança para modelos de formulário com código](how-to-configure-security-settings-for-form-templates-with-code.md)
    
## <a name="see-also"></a>Ver também

#### <a name="tasks"></a>Tarefas

[Definir configurações de segurança para modelos de formulário com código](how-to-configure-security-settings-for-form-templates-with-code.md)


[Sobre o modelo de segurança para modelos de formulário com código](about-the-security-model-for-form-templates-with-code.md)
  
[Visualizar e depurar modelos de formulário que exigem confiança total](how-to-preview-and-debug-form-templates-that-require-full-trust.md)

