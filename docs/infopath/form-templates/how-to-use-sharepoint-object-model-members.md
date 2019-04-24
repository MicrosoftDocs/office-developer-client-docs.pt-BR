---
title: Usar membros do modelo de objeto do SharePoint
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8cbafca3-7831-4231-8e61-38330b5ad61b
description: Antes de poder programar em membros do modelo de objeto do SharePoint a partir do código em execução em um modelo de formulário do InfoPath, você deve fazer referência ao assembly Microsoft. SharePoint. dll no projeto do Visual Studio 2012 para seu formulário. Para fazer isso, você deve ter acesso ao sistema de arquivos de uma cópia licenciada do Microsoft SharePoint Server 2010 ou de um servidor que esteja executando o Microsoft SharePoint Foundation 2010 para que você possa obter uma cópia do assembly Microsoft. SharePoint. dll.
ms.openlocfilehash: e29725450a6a1bdcba99215e337493f8686491e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303588"
---
# <a name="use-sharepoint-object-model-members"></a>Usar membros do modelo de objeto do SharePoint

Antes de poder programar em membros do modelo de objeto do SharePoint a partir do código em execução em um modelo de formulário do InfoPath, você deve fazer referência ao assembly Microsoft. SharePoint. dll no projeto do Visual Studio 2012 para seu formulário. Para fazer isso, você deve ter acesso ao sistema de arquivos de uma cópia licenciada do Microsoft SharePoint Server 2010 ou de um servidor que esteja executando o Microsoft SharePoint Foundation 2010 para que você possa obter uma cópia do assembly Microsoft. SharePoint. dll. 
  
Além disso, seu modelo de formulário deve ser implantado no servidor como uma solução de área restrita ou aprovada pelo administrador. Para obter mais informações sobre essas opções de implantação, consulte [publicAndo formulários com código](publishing-forms-with-code.md).
  
## <a name="add-and-reference-the-microsoftsharepoint-assembly-from-an-infopath-form-template"></a>Adicionar e referenciar o assembly Microsoft. SharePoint a partir de um modelo de formulário do InfoPath

> [!IMPORTANT]
> Para evitar um conflito com o modo como o sistema de projeto do InfoPath gerencia arquivos que são adicionados ao arquivo de modelo de formulário, não copie os assemblies que você deseja fazer referência à pasta de nível superior de um projeto de modelo de formulário. Por padrão, este será um caminho no seguinte formato: < *drive* >: \Users\ *username* \Documents\InfoPath Projects \ *NomeDoProjeto* > se você deseja mover assemblies que você referenciar para um local dentro da pasta do projeto, você deve criar uma subpasta na pasta do projeto *ProjectName* principal e, em seguida, copiar e fazer referência a assemblies dessa subpasta. No enTanto, lembre-se de que a criação de uma subpasta para assemblies referenciados não é necessária. Desde que um assembly referenciado não esteja localizado dentro da pasta de nível superior do projeto, o sistema de projeto do InfoPath copiará o assembly para o arquivo de modelo de formulário (. xsn) quando o projeto for compilado e publicado. 
  
Por padrão, o Microsoft. SharePoint. Server. dll é instalado em C:\Program Files\Common Files\Microsoft Shared\Web Server\Extensions\14\ISAPI no sistema de arquivos do SharePoint Server 2010 ou em um servidor que esteja executando o SharePoint Foundation 2010.
  
### <a name="to-reference-the-microsoftsharepoint-assembly-from-an-infopath-forms-code-project"></a>Para fazer referência à assembly Microsoft. SharePoint a partir de um projeto de código de formulário do InfoPath

1. Copie o assembly Microsoft. SharePoint. Server. dll do servidor para uma pasta local ou obtenha acesso ao assembly a partir de uma pasta compartilhada.
    
2. Abra o projeto de modelo de formulário no Visual Studio 2012.
    
3. On the **Project** menu, click **Add Reference**.
    
4. Clique na guia **procurar** , localize e especifique o assembly e, em seguida, clique em **OK** para adicionar a referência. 
    
Agora você pode escrever código em membros do modelo de objeto do SharePoint a partir do seu código de formulário. Para facilitar a referência de membros do namespace Microsoft. SharePoint, adicione `using Microsoft.SharePoint;` ou `Imports Microsoft.SharePoint` às diretivas no início do seu arquivo de código. Para obter um exemplo que mostra como usar membros do modelo de objeto do SharePoint em um formulário do InfoPath, consulte "exemplo 2: Gerenciando fornecedores em uma lista do SharePoint" em [soluções de área restrita de exemplo](sample-sandboxed-solutions.md).

