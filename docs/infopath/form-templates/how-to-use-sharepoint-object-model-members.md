---
title: Usar membros do modelo de objeto do SharePoint
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8cbafca3-7831-4231-8e61-38330b5ad61b
description: Antes de você pode programar membros do modelo de objeto do SharePoint a partir de código sendo executado em um modelo de formulário do InfoPath, você deve fazer referência a assembly Microsoft.SharePoint.dll no projeto do Visual Studio 2012 para o seu formulário. Para fazer isso, você deve ter acesso ao sistema de arquivos de uma cópia licenciada do Microsoft SharePoint Server 2010 ou um servidor que está executando o Microsoft SharePoint Foundation 2010 para que você possa obter uma cópia do assembly Microsoft.SharePoint.dll.
ms.openlocfilehash: c496f603f50a55ae2eaee237d6910d92612e1761
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765610"
---
# <a name="use-sharepoint-object-model-members"></a>Usar membros do modelo de objeto do SharePoint

Antes de você pode programar membros do modelo de objeto do SharePoint a partir de código sendo executado em um modelo de formulário do InfoPath, você deve fazer referência a assembly Microsoft.SharePoint.dll no projeto do Visual Studio 2012 para o seu formulário. Para fazer isso, você deve ter acesso ao sistema de arquivos de uma cópia licenciada do Microsoft SharePoint Server 2010 ou um servidor que está executando o Microsoft SharePoint Foundation 2010 para que você possa obter uma cópia do assembly Microsoft.SharePoint.dll. 
  
Além disso, o seu modelo de formulário deve ser implantado para o servidor como uma solução em área restrita ou aprovados pelo administrador. Para obter mais informações sobre essas opções de implantação, consulte [Publicando formulários com código](publishing-forms-with-code.md).
  
## <a name="add-and-reference-the-microsoftsharepoint-assembly-from-an-infopath-form-template"></a>Adicione e referência de Assembly do Microsoft a partir de um modelo de formulário do InfoPath

> [!IMPORTANT]
> Para evitar um conflito com como o sistema de projeto do InfoPath gerencia arquivos que são adicionados ao arquivo de modelo de formulário, não copie todos os assemblies que você deseja fazer referência para a pasta de nível superior de um projeto de modelo de formulário. Por padrão, este será um caminho no seguinte formato: < *unidade* >: \Users\ \Documents\InfoPath Projects\ *UserName* *NomeDoProjeto* > Se você deseja mover os assemblies que você faz referência a um local dentro da pasta do projeto, você Crie uma subpasta na pasta do projeto *NomeDoProjeto* principal e copie e assemblies de referência da subpasta. No entanto, lembre-se de que a criação de uma subpasta para assemblies referenciados não é necessário. Desde que um assembly referenciado não está localizado na pasta de nível superior do projeto, o sistema de projeto do InfoPath copiará o assembly para o arquivo de modelo de formulário (. xsn) quando o projeto é compilado e publicado. 
  
Por padrão, Microsoft.SharePoint.Server.dll é instalado em C:\Program Files\Common Files\Microsoft Shared\Web Server\Extensions\14\ISAPI no sistema de arquivos do SharePoint Server 2010 ou um servidor que está executando o SharePoint Foundation 2010.
  
### <a name="to-reference-the-microsoftsharepoint-assembly-from-an-infopath-forms-code-project"></a>Para fazer referência a assembly do Microsoft do projeto de código de um formulário do InfoPath

1. Copie o assembly Microsoft.SharePoint.Server.dll do servidor para uma pasta local ou obter acesso ao conjunto de uma pasta compartilhada.
    
2. Abra o projeto de modelo de formulário no Visual Studio 2012.
    
3. On the **Project** menu, click **Add Reference**.
    
4. Clique na guia **Procurar** , localize especificar o assembly e clique em **Okey** para adicionar a referência. 
    
Agora você pode escrever código contra membros do modelo de objeto do SharePoint do seu código de formulário. Para tornar mais fácil para os membros da referência do namespace Microsoft. SharePoint, adicione `using Microsoft.SharePoint;` ou `Imports Microsoft.SharePoint` às diretivas no início do seu arquivo de código. Para obter um exemplo que mostra como usar os membros do modelo de objeto do SharePoint em um formulário do InfoPath, consulte "Exemplo 2: Gerenciando fornecedores em uma lista do SharePoint" na [Amostra de soluções em área restrita](sample-sandboxed-solutions.md).

