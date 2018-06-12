---
title: Abrir ou converter um modelo de formulário criado com o Kit de ferramentas do InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- convertendo modelos de formulário [infopath 2007], InfoPath Toolkit, abrindo modelos de formulário de, abrindo o InfoPath 2007, convertendo modelos de formulário do InfoPath Toolkit, abrindo modelos de formulário [InfoPath 2007], modelos de formulário [InfoPath de modelos de formulário [InfoPath 2007] 2007], convertendo, script [InfoPath 2007], convertendo para código gerenciado
localization_priority: Normal
ms.assetid: af8eca2e-ba9a-4c37-94af-662815fff518
description: Se você criou um modelo de formulário de código gerenciado do InfoPath 2003 usando um dos kits de ferramentas do InfoPath 2003 para o Visual Studio e deseja manter a compatibilidade com o InfoPath 2003, você pode continuar a trabalhar e desenvolver ainda mais o seu projeto de modelo de formulário abrindo-o no Microsoft InfoPath e Visual Studio 2012.
ms.openlocfilehash: 7ca6a676c9db740b6b176783273a523715032387
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765623"
---
# <a name="open-or-convert-a-form-template-created-with-the-infopath-toolkit"></a>Abrir ou converter um modelo de formulário criado com o Kit de ferramentas do InfoPath

Se você criou um modelo de formulário de código gerenciado do InfoPath 2003 usando um dos kits de ferramentas do InfoPath 2003 para o Visual Studio e deseja manter a compatibilidade com o InfoPath 2003, você pode continuar a trabalhar e desenvolver ainda mais o seu projeto de modelo de formulário abrindo-o no Microsoft InfoPath e Visual Studio 2012.
  
Como alternativa, você pode migrar e atualizar o código no projeto do InfoPath 2003 para usar o novo modelo de objeto do .NET fornecido pelo namespace [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) . Ao fazer isso, todos os seus códigos precisará ser gravado novamente para usar os membros do namespace **Microsoft.Office.InfoPath** , mas todo o código do seu projeto anterior é mantido e envolta por **#if InfoPathManagedObjectModel** e **#endif **(C#) ou **Modelo de InfoPathManagedObject #If** e **#End se** (Visual Basic) instruções para referência. 
  
Os procedimentos a seguir descrevem como abrir um modelo de formulário de código gerenciado criado usando o InfoPath Toolkit e manter a compatibilidade com o InfoPath 2003 ou migrar e atualizar para o novo modelo de objeto do InfoPath. 
  
### <a name="open-a-managed-code-form-template-created-with-the-infopath-toolkit-and-maintain-compatibility-with-infopath-2003-using-visual-studio-tools-for-applications"></a>Abrir um modelo de formulário de código gerenciado criado com o InfoPath Toolkit e manter a compatibilidade com o InfoPath 2003 usando Visual Studio Tools for Applications

1. Abra o InfoPath Designer e clique em **Abrir** na guia **arquivo** . 
    
2. Na caixa de diálogo **Abrir no modo de Design** , navegue até a pasta onde o projeto de modelo de formulário do InfoPath Toolkit é salva do projeto. 
    
    Por padrão, isso será uma pasta no `C:\Users\` *username* `\Documents\Visual Studio Projects` no computador onde o projeto foi criado.   Ou, você pode mover a pasta para o local onde o InfoPath armazena os projetos do Visual Studio 2012, que, por padrão, é `C:\Users\` *username*  `\Documents\InfoPath Projects`
    
3. Clique no arquivo nomeado xsf e clique em **Abrir**.
    
4. Na guia **desenvolvedor** , clique em **Editor de código**.
    
5. A mensagem "Este modelo de formulário deve ser salvo antes de adicionar código Visual Basic ou c# a ele" é exibido. Clique em **Okey** para continuar. 
    
6. Navegue até o local onde deseja salvar o arquivo, nomeie o arquivo e clique em **Salvar**.
    
7. A mensagem "Este código foi criado com um dos InfoPath 2003 kits de ferramentas para Microsoft Visual Studio. O InfoPath precisa migrar o projeto do Kit de ferramentas em um novo formato"é exibida. Clique em **Okey** para continuar. 
    
8. Selecione o arquivo de solução do Visual Studio (. sln) para o projeto e clique em **Abrir**.
    
9. A mensagem "seu projeto foi migrado" é exibida quando o processo de migração for concluído. Clique em **Okey** para continuar. 
    
10. "O código neste formulário usa o modelo de objeto do InfoPath 2003" será exibida a mensagem com o prompt "Você deseja atualizar seu código para usar o modelo de objeto do Microsoft Office InfoPath?" Clique em **não** para manter a compatibilidade com o InfoPath 2003 e continuar a trabalhar com o modelo de objeto fornecido pelo namespace [SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) . 
    
    Para obter informações sobre como trabalhar com modelos de formulário de código gerenciado que são compatíveis com o InfoPath 2003, consulte a [Desenvolver modelos de formulário usando o modelo de objeto do InfoPath 2003](developing-form-templates-using-the-infopath-2003-object-model.md).
    
### <a name="open-a-managed-code-form-template-created-with-the-infopath-toolkit-and-upgrade-it-to-use-the-new-infopath-object-model-using-visual-studio-tools-for-applications"></a>Abrir um modelo de formulário de código gerenciado criados com o InfoPath Toolkit e atualizá-lo para usar o novo modelo de objeto do InfoPath usando o Visual Studio Tools for Applications

1. Abra o InfoPath Designer e clique em **Abrir** na guia **arquivo** . 
    
2. Em **Abrir um modelo de formulário**, clique **Em Meu computador**.
    
3. Na caixa de diálogo **Abrir no modo de Design** , navegue até a pasta onde o projeto de modelo de formulário do InfoPath Toolkit é salva do projeto. 
    
    Por padrão, isso será uma pasta no `C:\Users\` *username* `\Documents\Visual Studio Projects` no computador onde o projeto foi criado.   Ou, você pode mover a pasta para o local onde o InfoPath armazena os projetos do Visual Studio 2012, que, por padrão, é `C:\Users\` *username*  `\Documents\InfoPath Projects`
    
4. Clique no arquivo nomeado xsf e clique em **Abrir**.
    
5. Na guia **desenvolvedor** , clique em **Editor de código**.
    
6. A mensagem "Este modelo de formulário deve ser salvo antes de adicionar código Visual Basic ou c# a ele" é exibido. Clique em **Okey** para continuar. 
    
7. Navegue até o local onde deseja salvar o arquivo, nomeie o arquivo e clique em **Salvar**.
    
8. A mensagem "Este código foi criado com um dos InfoPath 2003 kits de ferramentas para Microsoft Visual Studio. O InfoPath precisa migrar o projeto do Kit de ferramentas em um novo formato"é exibida. Clique em **Okey** para continuar. 
    
9. Selecione o arquivo de solução do Visual Studio (. sln) para o projeto e clique em **Abrir**.
    
10. A mensagem "seu projeto foi migrado" é exibida quando o processo de migração for concluído. Clique em **Okey** para continuar. 
    
11. "O código neste formulário usa o modelo de objeto do InfoPath 2003" será exibida a mensagem com o prompt "Você deseja atualizar seu código para usar o modelo de objeto do Microsoft Office InfoPath?" Clique em **Sim** para atualizar o modelo de formulário para usar o novo modelo de objeto de código gerenciado fornecido pelo namespace [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) . 
    
    Seu código de formulário é aberto no editor de código do Visual Studio 2012 com todo o código do seu projeto anterior envolvido por **#if** **InfoPathManagedObjectModel** e **#endif** (c#) ou **#If InfoPathManagedObjectModel** e **#End se **Instruções (Visual Basic) para sua referência. Todo esse código terá que ser gravado novamente usar membros do modelo de objeto fornecidos pelo namespace **Microsoft.Office.InfoPath** . 
    
    Para obter informações sobre como trabalhar com modelos de formulário de código gerenciado que usam o novo modelo de objeto de código gerenciado do InfoPath, consulte [Desenvolver modelos de formulário do InfoPath com código](developing-infopath-form-templates-with-code.md).
    

