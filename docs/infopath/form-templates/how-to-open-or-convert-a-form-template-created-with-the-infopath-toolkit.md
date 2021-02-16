---
title: Abrir ou converter um modelo de formulário criado com o kit de ferramentas do InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- converting form templates [infopath 2007],InfoPath Toolkit, opening form templates from,form templates [InfoPath 2007], opening,InfoPath 2007, converting InfoPath Toolkit form templates,opening form templates [InfoPath 2007],form templates [InfoPath 2007], converting,script [InfoPath 2007], converting to managed code
localization_priority: Normal
ms.assetid: af8eca2e-ba9a-4c37-94af-662815fff518
description: Se você criou um modelo de formulário de código gerenciado do InfoPath 2003 usando um dos Kits de Ferramentas do InfoPath 2003 para Visual Studio e deseja manter a compatibilidade com o InfoPath 2003, pode continuar a trabalhar e desenvolver ainda mais seu projeto de modelo de formulário abrindo-o no Microsoft InfoPath e no Visual Studio 2012.
ms.openlocfilehash: 0acbfab4a83a71d94a1c70a667a963056f5b9a38
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428582"
---
# <a name="open-or-convert-a-form-template-created-with-the-infopath-toolkit"></a>Abrir ou converter um modelo de formulário criado com o Kit de ferramentas do InfoPath

Se você criou um modelo de formulário de código gerenciado do InfoPath 2003 usando um dos Kits de Ferramentas do InfoPath 2003 para Visual Studio e deseja manter a compatibilidade com o InfoPath 2003, pode continuar a trabalhar e desenvolver ainda mais seu projeto de modelo de formulário abrindo-o no Microsoft InfoPath e no Visual Studio 2012.
  
Como alternativa, você pode migrar e atualizar o código em seu projeto do InfoPath 2003 para usar o novo modelo de objeto .NET fornecido pelo namespace [Microsoft.Office.InfoPath.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) Ao fazer isso, todo o seu código precisará ser regravado para usar membros do namespace **Microsoft.Office.InfoPath,** mas todo o código do projeto anterior será mantido e rodeado por **instruções #if InfoPathManagedObjectModel** e **#endif** (C#) ou **#If InfoPathManagedObject Model** e instruções #End **If** (Visual Basic) para sua referência. 
  
Os procedimentos a seguir descrevem como abrir um modelo de formulário de código gerenciado criado usando o InfoPath Toolkit e manter a compatibilidade com o InfoPath 2003 ou migrar e atualizar para o novo modelo de objeto do InfoPath. 
  
### <a name="open-a-managed-code-form-template-created-with-the-infopath-toolkit-and-maintain-compatibility-with-infopath-2003-using-visual-studio-tools-for-applications"></a>Abrir um modelo de formulário de código gerenciado criado com o InfoPath Toolkit e manter a compatibilidade com o InfoPath 2003 usando o Visual Studio Tools for Applications

1. Abra o InfoPath Designer e clique em **Abrir** na **guia** Arquivo. 
    
2. Na caixa **de diálogo Abrir no Modo de Design,** navegue até a pasta do projeto onde o projeto de modelo de formulário do InfoPath Toolkit é salvo. 
    
    Por padrão, essa será uma pasta em nome de `C:\Users\`  `\Documents\Visual Studio Projects` usuário no computador onde o projeto foi criado.   Ou você pode mover a pasta para o local onde o InfoPath armazena projetos do Visual Studio 2012, que por padrão é o nome de  `C:\Users\` *usuário*  `\Documents\InfoPath Projects`
    
3. Clique no arquivo chamado manifest.xsf e clique em **Abrir.**
    
4. Na guia **Desenvolvedor,** clique em **Editor de Código.**
    
5. A mensagem "Este modelo de formulário deve ser salvo antes que você possa adicionar código do Visual Basic ou C# a ela" é exibida. Clique em **OK** para continuar. 
    
6. Navegue até o local onde deseja salvar o arquivo, nomee o arquivo e clique em **Salvar.**
    
7. A mensagem "Este código foi criado com um dos Kits de Ferramentas do InfoPath 2003 para o Microsoft Visual Studio. O InfoPath precisa migrar o projeto do kit de ferramentas para um novo formato" é exibido. Clique em **OK** para continuar. 
    
8. Selecione o arquivo de solução do Visual Studio (.sln) para o projeto e clique em **Abrir**.
    
9. A mensagem "Seu projeto foi migrado" é exibida quando o processo de migração é concluído. Clique em **OK** para continuar. 
    
10. A mensagem "O código neste formulário usa o modelo de objeto do InfoPath 2003" é exibida com o prompt "Você deseja atualizar seu código para usar o modelo de objeto do Microsoft Office InfoPath?" Clique **em Não** para manter a compatibilidade com o InfoPath 2003 e para continuar trabalhando com o modelo de objeto fornecido pelo namespace [Microsoft.Office.Interop.InfoPath.SemiTrust.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) 
    
    Para obter informações sobre como trabalhar com modelos de formulário de código gerenciado compatíveis com o InfoPath 2003, consulte Developing [Form Templates Using the InfoPath 2003 Object Model](developing-form-templates-using-the-infopath-2003-object-model.md).
    
### <a name="open-a-managed-code-form-template-created-with-the-infopath-toolkit-and-upgrade-it-to-use-the-new-infopath-object-model-using-visual-studio-tools-for-applications"></a>Abra um modelo de formulário de código gerenciado criado com o InfoPath Toolkit e atualize-o para usar o novo modelo de objeto do InfoPath usando o Visual Studio Tools for Applications

1. Abra o InfoPath Designer e clique em **Abrir** na **guia** Arquivo. 
    
2. Em **Abrir um modelo de formulário,** clique em Meu **Computador.**
    
3. Na caixa **de diálogo Abrir no Modo de Design,** navegue até a pasta do projeto onde o projeto de modelo de formulário do InfoPath Toolkit é salvo. 
    
    Por padrão, será uma pasta em nome `C:\Users\` *de* `\Documents\Visual Studio Projects` usuário no computador onde o projeto foi criado.   Ou você pode mover a pasta para o local onde o InfoPath armazena projetos do Visual Studio 2012, que por padrão é o nome de  `C:\Users\` *usuário*  `\Documents\InfoPath Projects`
    
4. Clique no arquivo chamado manifest.xsf e clique em **Abrir.**
    
5. Na guia **Desenvolvedor,** clique em **Editor de Código.**
    
6. A mensagem "Este modelo de formulário deve ser salvo antes que você possa adicionar código do Visual Basic ou C# a ela" é exibida. Clique em **OK** para continuar. 
    
7. Navegue até o local onde deseja salvar o arquivo, nomee o arquivo e clique em **Salvar.**
    
8. A mensagem "Este código foi criado com um dos Kits de Ferramentas do InfoPath 2003 para o Microsoft Visual Studio. O InfoPath precisa migrar o projeto do kit de ferramentas para um novo formato" é exibido. Clique em **OK** para continuar. 
    
9. Selecione o arquivo de solução do Visual Studio (.sln) para o projeto e clique em **Abrir**.
    
10. A mensagem "Seu projeto foi migrado" é exibida quando o processo de migração é concluído. Clique em **OK** para continuar. 
    
11. A mensagem "O código neste formulário usa o modelo de objeto do InfoPath 2003" é exibida com o prompt "Você deseja atualizar seu código para usar o modelo de objeto do Microsoft Office InfoPath?" Clique **em Sim** para atualizar o modelo de formulário para usar o novo modelo de objeto de código gerenciado fornecido pelo namespace [Microsoft.Office.InfoPath.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 
    
    Seu código de formulário é aberto no editor de código do Visual Studio 2012 com todo o código do projeto anterior rodeado por **instruções #if** **InfoPathManagedObjectModel** e **#endif** (C#) ou **#If InfoPathManagedObjectModel** e instruções #End **If** (Visual Basic) para sua referência. Todo esse código terá que ser rees gravado para usar membros do modelo de objeto fornecido pelo namespace **Microsoft.Office.InfoPath.** 
    
    Para saber mais sobre como trabalhar com modelos de formulário de código gerenciado que usam o novo modelo de objeto de código gerenciado do InfoPath, confira Desenvolver modelos de formulário do [InfoPath com código.](developing-infopath-form-templates-with-code.md)
    

