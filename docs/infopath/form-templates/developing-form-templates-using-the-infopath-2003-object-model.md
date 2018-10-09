---
title: Desenvolver modelos de formulário usando o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- modelos de formulário [infopath 2007], usar o modelo de objeto do infopath 2003, modelos de formulário compatíveis com InfoPath 2003,InfoPath 2007, desenvolver modelos de formulário usando o modelo de objeto do InfoPath 2003, modelos de objeto [InfoPath 2003], desenvolver modelos de formulário com código gerenciado
localization_priority: Normal
ms.assetid: c74cbcd0-4fe6-4eb7-a05c-f61e1868c42b
description: O Microsoft InfoPath continua oferecendo suporte a projetos de modelos de formulário criados com o Kit de Ferramentas do InfoPath 2003 do Microsoft Office para as ferramentas do Visual Studio .NET ou do Visual Studio 2005 do sistema Microsoft Office que possuem lógica que negócios escrita contra membros do namespace Microsoft.Office.Interop.InfoPath.SemiTrust. Os tópicos desta seção referem-se aos tipos e membros deste namespace, como o modelo de objeto compatível com InfoPath 2003, ou simplesmente o modelo de objeto do InfoPath 2003. O InfoPath também dá suporte a projetos de modelo de formulário criados no Microsoft Office InfoPath 2007 que usam o modelo de objeto compatível com o InfoPath 2003. Adicionalmente, você pode usar o InfoPath para criar novos projetos de modelos de formulário que usam o modelo de objeto compatível com o InfoPath 2003 para manter a compatibilidade com versões anteriores para usuários do Office InfoPath 2007. Todos os tópicos desta seção são específicos para a criação e o desenvolvimento de modelos de formulário que funcionam com o modelo de objeto compatível com o InfoPath 2003 fornecido pelo namespace Microsoft.Office.Interop.InfoPath.SemiTrust.
ms.openlocfilehash: a39f921f6c7465dbcf469062b866c808fa222851
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401409"
---
# <a name="developing-form-templates-using-the-infopath-2003-object-model"></a>Desenvolver modelos de formulário usando o modelo de objeto do InfoPath 2003

O Microsoft InfoPath continua oferecendo suporte a projetos de modelos de formulário criados com o Kit de Ferramentas do InfoPath 2003 do Microsoft Office para as ferramentas do Visual Studio .NET ou do Visual Studio 2005 do sistema Microsoft Office que possuem lógica que negócios escrita contra membros do namespace [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx). Os tópicos desta seção referem-se aos tipos e membros deste namespace, como o modelo de objeto compatível com InfoPath 2003, ou simplesmente o modelo de objeto do InfoPath 2003. O InfoPath também dá suporte a projetos de modelo de formulário criados no Microsoft Office InfoPath 2007 que usam o modelo de objeto compatível com o InfoPath 2003. Adicionalmente, você pode usar o InfoPath para criar novos projetos de modelos de formulário que usam o modelo de objeto compatível com o InfoPath 2003 para manter a compatibilidade com versões anteriores para usuários do Office InfoPath 2007. Todos os tópicos desta seção são específicos para a criação e o desenvolvimento de modelos de formulário que funcionam com o modelo de objeto compatível com o InfoPath 2003 fornecido pelo namespace [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx). 
  
> [!IMPORTANT]
> Embora a criação de lógicas de negócios com o modelo de objeto com código gerenciado fornecido pelo namespace [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) ainda seja suportada pela lógica de negócios escrita do InfoPath usando este modelo de objeto, ela não é suportada por modelos de formulário habilitados para navegador implantados no Microsoft SharePoint Server 2010 com InfoPath Forms Services. Modelos de formulário habilitados para navegador devem usar o novo modelo de objeto com código gerenciado do InfoPath fornecido pelos membros do [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) para lógica de negócios personalizada. Para saber mais sobre como criar modelos de formulário com lógica de negócios escrita com membros do namespace [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx), confira [Desenvolvimento de Modelos de Formulário do InfoPath com Código](developing-infopath-form-templates-with-code.md). > Além disso, observe que os usuários de modelos de formulário compilados com Visual Studio 2012 devem ter o Microsoft .NET Framework 2.0 ou uma versão posterior instalados em seus computadores. Os usuários de modelos de formulário compilados com Visual Studio .NET 2003 só precisarão ter o Microsoft .NET Framework 1.1 em seus computadores. 
  
## <a name="in-this-section"></a>Nesta seção

[Introdução ao desenvolvimento de modelos de formulário usando o modelo de objeto do InfoPath 2003](get-started-developing-form-templates-using-infopath-object-model.md)
  
> Fornece informações sobre como começar a criar modelos de formulário com código gerenciado que funcionam com o modelo de objeto compatível com o InfoPath 2003.
    
[Criar modelos de formulário usando o modelo de objeto do InfoPath 2003](creating-form-templates-using-the-infopath-2003-object-model.md)
  
> Discute a inicialização e o código de limpeza, como adicionar manipuladores de eventos, como depurar e implantar modelos de formulário com código gerenciado, suporte a conversas e o trabalho com Microsoft XML Core Services (MSXML) de soluções de código gerenciado do InfoPath.
    
[Segurança nos modelos de formulário do InfoPath com código](security-in-infopath-form-templates-with-code.md)
  
> Descreve o modelo de segurança para modelos de formulário do InfoPath que usam código gerenciado, depuração totalmente confiável de modelos de formulário do InfoPath e procedimentos de segurança relacionados.
    
[Compreender o modelo de objeto do InfoPath 2003](understanding-the-infopath-2003-object-model.md)
  
> Discute o modelo de objeto compatível com o InfoPath 2003 e tarefas comuns de programação para modelos de formulário com código gerenciado que funcionam com esse modelo de objeto.
    
[Resolver problemas de modelos de formulário que usam o modelo de objeto do InfoPath 2003](troubleshoot-form-templates-that-use-infopath-object-model.md)
  
> Contém dicas para resolver problemas comuns que podem ocorrer durante a criação de modelos de formulário com código gerenciado que funcionam com o modelo de objeto compatível com o InfoPath 2003.
    
## <a name="related-sections"></a>Seções relacionadas

[Portal de desenvolvedor do InfoPath](https://go.microsoft.com/fwlink?LinkID=11689)
  
> Contém links para artigos técnicos, amostras de código, downloads, suporte e outros documentos de MSDN sobre a criação de soluções personalizadas do InfoPath.
    
[Central de Desenvolvedores do Microsoft Office](https://go.microsoft.com/fwlink?LinkID=27128)
  
> Contém links para artigos técnicos, amostras de código, downloads, suporte e outros documentos de MSDN sobre a criação de soluções personalizadas do Office.
    

