---
title: Usar membros do modelo de objeto do SharePoint
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8cbafca3-7831-4231-8e61-38330b5ad61b
description: Antes de poder programar em relação aos membros do modelo de objeto do SharePoint do código em execução em um modelo de formulário do InfoPath, você deve fazer referência ao assembly Microsoft.SharePoint.dll no projeto do Visual Studio 2012 para seu formulário. Para fazer isso, você deve ter acesso ao sistema de arquivos de uma cópia licenciada do Microsoft SharePoint Server 2010 ou de um servidor que está executando o Microsoft SharePoint Foundation 2010 para que você possa obter uma cópia do assembly Microsoft.SharePoint.dll.
ms.openlocfilehash: e29725450a6a1bdcba99215e337493f8686491e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431656"
---
# <a name="use-sharepoint-object-model-members"></a>Usar membros do modelo de objeto do SharePoint

Antes de poder programar em relação aos membros do modelo de objeto do SharePoint do código em execução em um modelo de formulário do InfoPath, você deve fazer referência ao assembly Microsoft.SharePoint.dll no projeto do Visual Studio 2012 para seu formulário. Para fazer isso, você deve ter acesso ao sistema de arquivos de uma cópia licenciada do Microsoft SharePoint Server 2010 ou de um servidor que está executando o Microsoft SharePoint Foundation 2010 para que você possa obter uma cópia do assembly Microsoft.SharePoint.dll. 
  
Além disso, seu modelo de formulário deve ser implantado no servidor como uma solução de área de segurança ou aprovada pelo administrador. Para obter mais informações sobre essas opções de implantação, consulte [Formulários de Publicação com Código.](publishing-forms-with-code.md)
  
## <a name="add-and-reference-the-microsoftsharepoint-assembly-from-an-infopath-form-template"></a>Adicionar e fazer referência ao assembly Microsoft.SharePoint de um modelo de formulário do InfoPath

> [!IMPORTANT]
> Para evitar um conflito com a forma como o sistema de projeto do InfoPath gerencia arquivos adicionados ao arquivo de modelo de formulário, não copie nenhum assemblies que você deseja referenciar na pasta de nível superior de um projeto de modelo de formulário. Por padrão, este será um caminho no seguinte formato: *<*  unidade >:\Users\  *UserName*  \Documents\InfoPath Projects\  *ProjectName* > Se você deseja mover assemblies que você faz referência a um local dentro da pasta do projeto, você deve criar uma subpasta sob a pasta principal do projeto  *ProjectName*  e, em seguida, copiar e referenciar assemblies dessa subpasta. No entanto, esteja ciente de que não é necessário criar uma subpasta para assemblies referenciados. Enquanto um assembly referenciado não estiver localizado na pasta de nível superior do projeto, o sistema de projeto do InfoPath copiará o assembly para o arquivo de modelo de formulário (.xsn) quando o projeto for compilado e publicado. 
  
Por padrão, o Microsoft.SharePoint.Server.dll é instalado em C:\Program Files\Common Files\Microsoft Shared\Web Server\Extensions\14\ISAPI no sistema de arquivos do SharePoint Server 2010 ou em um servidor que está executando o SharePoint Foundation 2010.
  
### <a name="to-reference-the-microsoftsharepoint-assembly-from-an-infopath-forms-code-project"></a>Para fazer referência ao assembly Microsoft.SharePoint do projeto de código de um formulário do InfoPath

1. Copie o Microsoft.SharePoint.Server.dll assembly do servidor para uma pasta local ou acesse o assembly de uma pasta compartilhada.
    
2. Abra o projeto de modelo de formulário no Visual Studio 2012.
    
3. On the **Project** menu, click **Add Reference**.
    
4. Clique na **guia** Procurar, localize e especifique o assembly e clique em **OK** para adicionar a referência. 
    
Agora você pode escrever código em membros do modelo de objeto do SharePoint do seu código de formulário. Para facilitar a referência de membros do namespace Microsoft.SharePoint, adicione ou as diretivas no início  `using Microsoft.SharePoint;`  `Imports Microsoft.SharePoint` do arquivo de código. For an example that shows how to use members of the SharePoint object model in an InfoPath form, see "Example 2: Managing Vendors in a SharePoint List" in [Sample Sandboxed Solutions](sample-sandboxed-solutions.md).

