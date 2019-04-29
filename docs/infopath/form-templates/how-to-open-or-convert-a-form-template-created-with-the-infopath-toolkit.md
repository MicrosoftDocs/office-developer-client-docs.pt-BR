---
title: Abrir ou converter um modelo de formulário criado com o kit de ferramentas do InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Convertendo modelos de formulário [InfoPath 2007], kit de ferramentas do InfoPath, abrindo modelos de formulário do, modelos de formulário [InfoPath 2007], abrindo, InfoPath 2007, convertendo modelos de formulário do kit de ferramentas do InfoPath, abrindo modelos de formulário [InfoPath 2007], modelos de formulário [InfoPath 2007], convertendo, script [InfoPath 2007], convertendo em código gerenciado
localization_priority: Normal
ms.assetid: af8eca2e-ba9a-4c37-94af-662815fff518
description: Se você criou um modelo de formulário de código gerenciado do InfoPath 2003 usando um dos conjuntos de informações do InfoPath 2003 para Visual Studio e deseja manter a compatibilidade com o InfoPath 2003, poderá continuar a trabalhar e desenvolver ainda mais seu projeto de modelo de formulário abrindo-o em Microsoft InfoPath e Visual Studio 2012.
ms.openlocfilehash: 0acbfab4a83a71d94a1c70a667a963056f5b9a38
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428582"
---
# <a name="open-or-convert-a-form-template-created-with-the-infopath-toolkit"></a>Abrir ou converter um modelo de formulário criado com o kit de ferramentas do InfoPath

Se você criou um modelo de formulário de código gerenciado do InfoPath 2003 usando um dos conjuntos de informações do InfoPath 2003 para Visual Studio e deseja manter a compatibilidade com o InfoPath 2003, poderá continuar a trabalhar e desenvolver ainda mais seu projeto de modelo de formulário abrindo-o em Microsoft InfoPath e Visual Studio 2012.
  
Como alternativa, você pode migrar e atualizar o código no seu projeto do InfoPath 2003 para usar o novo modelo de objeto do .NET fornecido pelo namespace [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) . Ao fazer isso, todo o seu código precisará ser reescrito para usar membros do namespace **Microsoft. Office. InfoPath** , mas todo o código do seu projeto anterior é mantido e circundado por **#if InfoPathManagedObjectModel** e **#endif **(C#) ou **#If modelo InfoPathManagedObject** e **#End se** (Visual Basic) instruções para sua referência. 
  
Os procedimentos a seguir descrevem como abrir um modelo de formulário de código gerenciado criado usando o kit de ferramentas do InfoPath e manter a compatibilidade com o InfoPath 2003 ou migrar e atualizar para o novo modelo de objeto do InfoPath. 
  
### <a name="open-a-managed-code-form-template-created-with-the-infopath-toolkit-and-maintain-compatibility-with-infopath-2003-using-visual-studio-tools-for-applications"></a>Abrir um modelo de formulário de código gerenciado criado com o kit de ferramentas do InfoPath e manter a compatibilidade com o InfoPath 2003 usando o Visual Studio Tools for Applications

1. Abra o designer do InfoPath e, em seguida, clique em **abrir** na guia **arquivo** . 
    
2. Na caixa de diálogo **abrir no modo de design** , navegue até a pasta do projeto onde o projeto de modelo de formulário do kit de ferramentas do InfoPath foi salvo. 
    
    Por padrão, essa será uma pasta em `C:\Users\` *nome de usuário* `\Documents\Visual Studio Projects` no computador onde o projeto foi criado.   ou você pode mover a pasta para o local onde o InfoPath armazena projetos do Visual Studio 2012, que por padrão `C:\Users\` é *username*  `\Documents\InfoPath Projects`
    
3. Clique no arquivo chamado manifest. xsf e, em seguida, clique em **abrir**.
    
4. Na guia **desenvolvedor** , clique em **Editor de código**.
    
5. A mensagem "este modelo de formulário deve ser salvo para que você possa adicionar o código do Visual Basic ou C# a ele" é exibido. Clique em **OK** para continuar. 
    
6. Navegue até o local onde deseja salvar o arquivo, nomeie o arquivo e clique em **salvar**.
    
7. A mensagem "este código foi criado com um dos kits de mensagens do InfoPath 2003 para o Microsoft Visual Studio. O InfoPath precisa migrar o projeto do kit de ferramentas para um novo formato "é exibido. Clique em **OK** para continuar. 
    
8. Selecione o arquivo de solução do Visual Studio (. sln) para o projeto e clique em **abrir**.
    
9. A mensagem "o projeto foi migrado" é exibida quando o processo de migração é concluído. Clique em **OK** para continuar. 
    
10. A mensagem "o código neste formulário usa o modelo de objeto do InfoPath 2003" é exibido com o prompt "você deseja atualizar seu código para usar o modelo de objeto do Microsoft Office InfoPath?" Clique em **não** para manter a compatibilidade com o InfoPath 2003 e para continuar trabalhando com o modelo de objeto fornecido pelo namespace [Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) . 
    
    Para obter informações sobre como trabalhar com modelos de formulário de código gerenciado que são compatíveis com o InfoPath 2003, consulte [desenvolver modelos de formulário usando o modelo de objeto do InfoPath 2003](developing-form-templates-using-the-infopath-2003-object-model.md).
    
### <a name="open-a-managed-code-form-template-created-with-the-infopath-toolkit-and-upgrade-it-to-use-the-new-infopath-object-model-using-visual-studio-tools-for-applications"></a>Abrir um modelo de formulário de código gerenciado criado com o kit de ferramentas do InfoPath e atualizá-lo para usar o novo modelo de objeto do InfoPath usando o Visual Studio Tools for Applications

1. Abra o designer do InfoPath e, em seguida, clique em **abrir** na guia **arquivo** . 
    
2. Em **abrir um modelo de formulário**, clique **em meu computador**.
    
3. Na caixa de diálogo **abrir no modo de design** , navegue até a pasta do projeto onde o projeto de modelo de formulário do kit de ferramentas do InfoPath foi salvo. 
    
    Por padrão, essa será uma pasta em `C:\Users\` *nome de usuário* `\Documents\Visual Studio Projects` no computador onde o projeto foi criado.   ou você pode mover a pasta para o local onde o InfoPath armazena projetos do Visual Studio 2012, que por padrão `C:\Users\` é *username*  `\Documents\InfoPath Projects`
    
4. Clique no arquivo chamado manifest. xsf e, em seguida, clique em **abrir**.
    
5. Na guia **desenvolvedor** , clique em **Editor de código**.
    
6. A mensagem "este modelo de formulário deve ser salvo para que você possa adicionar o código do Visual Basic ou C# a ele" é exibido. Clique em **OK** para continuar. 
    
7. Navegue até o local onde deseja salvar o arquivo, nomeie o arquivo e clique em **salvar**.
    
8. A mensagem "este código foi criado com um dos kits de mensagens do InfoPath 2003 para o Microsoft Visual Studio. O InfoPath precisa migrar o projeto do kit de ferramentas para um novo formato "é exibido. Clique em **OK** para continuar. 
    
9. Selecione o arquivo de solução do Visual Studio (. sln) para o projeto e clique em **abrir**.
    
10. A mensagem "o projeto foi migrado" é exibida quando o processo de migração é concluído. Clique em **OK** para continuar. 
    
11. A mensagem "o código neste formulário usa o modelo de objeto do InfoPath 2003" é exibido com o prompt "você deseja atualizar seu código para usar o modelo de objeto do Microsoft Office InfoPath?" Clique em **Sim** para atualizar o modelo de formulário para usar o novo modelo de objeto de código gerenciado fornecido pelo namespace [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) . 
    
    Seu código de formulário é aberto no editor de código do Visual Studio 2012 com todo o código do projeto anterior envolvido por **#if** **InfoPathManagedObjectModel** e **#endif** (C#) ou **#If InfoPathManagedObjectModel** e **#End se **(Visual Basic) instruções para sua referência. Todo esse código terá que ser reescrito para usar membros do modelo de objeto fornecido pelo namespace **Microsoft. Office. InfoPath** . 
    
    Para obter informações sobre como trabalhar com modelos de formulário de código gerenciado que usam o novo modelo de objeto de código gerenciado do InfoPath, consulte [developIng InfoPath Form Templates with Code](developing-infopath-form-templates-with-code.md).
    

