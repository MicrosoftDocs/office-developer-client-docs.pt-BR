---
title: Desenvolver modelos de formulário usando o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- '[infopath 2007], de modelos de formulário usando o objeto do infopath 2003 modelar, modelos de formulário compatíveis com o InfoPath 2003, InfoPath 2007, desenvolvimento de modelos usando o modelo de objeto do InfoPath 2003, modelos de formulário de código gerenciado do desenvolvimento de modelos de objeto [InfoPath 2003], do formulário'
localization_priority: Normal
ms.assetid: c74cbcd0-4fe6-4eb7-a05c-f61e1868c42b
description: Microsoft InfoPath continua a oferecer suporte a projetos de modelo de formulário criados com o Microsoft Office InfoPath 2003 Toolkit para o Visual Studio .NET ou do Visual Studio 2005 Tools para o Microsoft Office System com lógica de negócios gravadas em relação a membros do Namespace SemiTrust. Os tópicos desta seção consultem os tipos de membros deste namespace como o modelo de objeto compatível com o InfoPath 2003 ou simplesmente o modelo de objeto do InfoPath 2003. InfoPath também oferece suporte a projetos de modelo de formulário criados com o Microsoft Office InfoPath 2007 que usam o modelo de objeto compatível com o InfoPath 2003. Além disso, você pode usar o InfoPath para criar o novo formulário projetos do modelo que usam o modelo de objeto do InfoPath 2003 compatíveis para manter a compatibilidade com versões anteriores para os usuários do Office InfoPath 2007. Todos os tópicos desta seção são específicos para a criação e desenvolvimento de modelos de formulário que funcionam com o modelo de objeto do InfoPath 2003 compatíveis fornecido pelo namespace SemiTrust.
ms.openlocfilehash: 5d949242068586c752e7a92fa53792cda9ececea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765588"
---
# <a name="developing-form-templates-using-the-infopath-2003-object-model"></a>Desenvolver modelos de formulário usando o modelo de objeto do InfoPath 2003

Microsoft InfoPath continua a oferecer suporte a projetos de modelo de formulário criados com o Microsoft Office InfoPath 2003 Toolkit para o Visual Studio .NET ou do Visual Studio 2005 Tools para o Microsoft Office System com lógica de negócios gravadas em relação a membros do [ SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace. Os tópicos desta seção consultem os tipos de membros deste namespace como o modelo de objeto compatível com o InfoPath 2003 ou simplesmente o modelo de objeto do InfoPath 2003. InfoPath também oferece suporte a projetos de modelo de formulário criados com o Microsoft Office InfoPath 2007 que usam o modelo de objeto compatível com o InfoPath 2003. Além disso, você pode usar o InfoPath para criar o novo formulário projetos do modelo que usam o modelo de objeto do InfoPath 2003 compatíveis para manter a compatibilidade com versões anteriores para os usuários do Office InfoPath 2007. Todos os tópicos desta seção são específicos para a criação e desenvolvimento de modelos de formulário que funcionam com o modelo de objeto do InfoPath 2003 compatíveis fornecido pelo namespace [SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) . 
  
> [!IMPORTANT]
> Embora a criação de lógica de negócios com o modelo de objeto de código gerenciado fornecido pelo namespace [SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) ainda é aceita pelo InfoPath, lógica comercial gravada usando esse modelo de objeto não é suportado para modelos de formulário habilitados para navegador implantados para Microsoft SharePoint Server 2010 com o InfoPath Forms Services. Modelos de formulário habilitados para navegador devem usar o novo modelo de objeto de código gerenciado do InfoPath fornecido pelos membros do namespace [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) para a lógica de negócios personalizado. Para obter mais informações sobre a criação de modelos de formulário com lógica de negócios gravadas com membros do namespace [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) , consulte [Desenvolver modelos de formulário do InfoPath com código](developing-infopath-form-templates-with-code.md). > Além disso, observe que os usuários de modelos de formulário compilados com o Visual Studio 2012 devem ter o Microsoft .NET Framework 2.0 ou posterior instalado em seus computadores. Os usuários de modelos de formulário compilados com o Visual Studio .NET 2003 somente precisarão ter o Microsoft .NET Framework 1.1 em seus computadores. 
  
## <a name="in-this-section"></a>Nesta seção

[Introdução ao desenvolvimento de modelos de formulário usando o modelo de objeto do InfoPath 2003](get-started-developing-form-templates-using-infopath-object-model.md)
  
> Fornece informações sobre como começar a criação de modelos de formulário que funcionam com o modelo de objeto do InfoPath 2003 compatíveis de código gerenciado.
    
[Criar modelos de formulário usando o modelo de objeto do InfoPath 2003](creating-form-templates-using-the-infopath-2003-object-model.md)
  
> Discute a inicialização e o código de limpeza, como adicionar manipuladores de eventos, como depurar e implantar modelos de formulário de código gerenciado, suporte a segmentação e trabalhando com o Microsoft XML Core Services (MSXML) de soluções de código gerenciado do InfoPath.
    
[Segurança nos modelos de formulário do InfoPath com código](security-in-infopath-form-templates-with-code.md)
  
> Discute o modelo de segurança para os modelos de formulário do InfoPath que usar o código gerenciado, depurando totalmente confiáveis InfoPath modelos de formulário e relacionadas a procedimentos de segurança.
    
[Compreender o modelo de objeto do InfoPath 2003](understanding-the-infopath-2003-object-model.md)
  
> Aborda o modelo de objeto do InfoPath 2003 compatíveis e tarefas de programação comuns para modelos de formulário de código gerenciado que funcionam com esse modelo de objeto.
    
[Resolver problemas de modelos de formulário usando o modelo de objeto do InfoPath 2003](troubleshoot-form-templates-that-use-infopath-object-model.md)
  
> Contém dicas para solucionar problemas comuns que você pode encontrar ao criar modelos de formulário de código gerenciado que funcionam com o modelo de objeto do InfoPath 2003 compatíveis.
    
## <a name="related-sections"></a>Se��es relacionadas

[Portal do desenvolvedor do InfoPath](http://go.microsoft.com/fwlink?LinkID=11689)
  
> Contém links para exemplos de código, artigos técnicos, downloads, suporte e outras documentações do MSDN sobre como criar soluções personalizadas do InfoPath.
    
[Centro de Desenvolvimento do Microsoft Office](http://go.microsoft.com/fwlink?LinkID=27128)
  
> Contém links para exemplos de código, artigos técnicos, downloads, suporte e outras documentações do MSDN sobre como criar soluções personalizadas do Office.
    

