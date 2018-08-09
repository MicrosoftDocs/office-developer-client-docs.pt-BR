---
title: Adicionar e fazer referência a assemblies personalizados
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- modelo de objeto de modelos de formulário de 2003 compatíveis do InfoPath, usando assemblies personalizados, assemblies [InfoPath 2007], adição personalizada usando o InfoPath 2003
localization_priority: Normal
ms.assetid: 20e1f43e-8279-48fc-8f34-16a2729dbc9b
description: Quando você adiciona uma referência a um assembly personalizado em um projeto de modelo de formulário de código gerenciado, nesse assembly é incluído dentro do arquivo de modelo de formulário (. xsn) quando o projeto é compilado e publicado.
ms.openlocfilehash: e182930ebe14b6f64d1b90509fe400cc1fb1b26e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765599"
---
# <a name="add-and-reference-custom-assemblies"></a><span data-ttu-id="e6865-104">Adicionar e fazer referência a assemblies personalizados</span><span class="sxs-lookup"><span data-stu-id="e6865-104">Add and Reference Custom Assemblies</span></span>

<span data-ttu-id="e6865-105">Quando você adiciona uma referência a um assembly personalizado em um projeto de modelo de formulário de código gerenciado, nesse assembly é incluído dentro do arquivo de modelo de formulário (. xsn) quando o projeto é compilado e publicado.</span><span class="sxs-lookup"><span data-stu-id="e6865-105">When you add a reference to a custom assembly in a managed-code form template project, that assembly is included within the form template file (.xsn) when your project is compiled and published.</span></span>
  
## <a name="add-and-reference-a-custom-assembly"></a><span data-ttu-id="e6865-106">Adicionar e fazer referência a um Assembly personalizado</span><span class="sxs-lookup"><span data-stu-id="e6865-106">Add and Reference a Custom Assembly</span></span>

<span data-ttu-id="e6865-107">Para evitar um conflito com como o sistema de projeto do InfoPath gerencia arquivos que são adicionados ao arquivo de modelo de formulário, não copie qualquer assemblies personalizados que você deseja fazer referência para a pasta de nível superior de um projeto de modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="e6865-107">To avoid a conflict with how the InfoPath project system manages files that are added to the form template file, do not copy any custom assemblies that you want to reference into the top-level folder of a form template project.</span></span> <span data-ttu-id="e6865-108">Por padrão, este será um caminho no seguinte formato: < *unidade* >: \Users\ \Documents\InfoPath Projects\ *UserName* *NomeDoProjeto*</span><span class="sxs-lookup"><span data-stu-id="e6865-108">By default, this will be a path in the following format: < *drive*  >:\Users\  *UserName*  \Documents\InfoPath Projects\  *ProjectName*</span></span> 
  
<span data-ttu-id="e6865-109">Se desejar mover assemblies personalizados que você faz referência a um local dentro da pasta do projeto, você deve criar uma subpasta na pasta do projeto principal e copie e assemblies personalizados de referência da subpasta.</span><span class="sxs-lookup"><span data-stu-id="e6865-109">If you do want to move custom assemblies that you reference to a location within the project folder, you must create a subfolder under the main project folder, and then copy and reference custom assemblies from that subfolder.</span></span> <span data-ttu-id="e6865-110">No entanto, lembre-se de que a criação de uma subpasta para assemblies referenciados não é necessário.</span><span class="sxs-lookup"><span data-stu-id="e6865-110">However, be aware that creating a subfolder for referenced assemblies is not necessary.</span></span> <span data-ttu-id="e6865-111">Desde que um assembly referenciado não está localizado na pasta de nível superior do projeto, o sistema de projeto do InfoPath copiará o assembly para o arquivo de modelo de formulário (. xsn) quando o projeto é compilado e publicado.</span><span class="sxs-lookup"><span data-stu-id="e6865-111">As long as a referenced assembly is not located within the project's top-level folder, the InfoPath project system will copy the assembly into the form template file (.xsn) when the project is compiled and published.</span></span>
  
### <a name="reference-a-custom-assembly-from-its-default-location"></a><span data-ttu-id="e6865-112">Referência a um assembly personalizado do local padrão</span><span class="sxs-lookup"><span data-stu-id="e6865-112">Reference a custom assembly from its default location</span></span>

1. <span data-ttu-id="e6865-113">Abra o projeto de modelo de formulário no Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="e6865-113">Open the form template project in Visual Studio 2012.</span></span>
    
2. <span data-ttu-id="e6865-114">On the **Project** menu, click **Add Reference**.</span><span class="sxs-lookup"><span data-stu-id="e6865-114">On the **Project** menu, click **Add Reference**.</span></span>
    
3. <span data-ttu-id="e6865-115">Clique na guia **Procurar** , localize especificar o assembly e clique em **Okey** para adicionar a referência.</span><span class="sxs-lookup"><span data-stu-id="e6865-115">Click the **Browse** tab, locate and specify the assembly, and then click **OK** to add the reference.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e6865-116">Ver também</span><span class="sxs-lookup"><span data-stu-id="e6865-116">See also</span></span>

#### <a name="tasks"></a><span data-ttu-id="e6865-117">Tarefas</span><span class="sxs-lookup"><span data-stu-id="e6865-117">Tasks</span></span>

[<span data-ttu-id="e6865-118">Criar um modelo de formulário usando o modelo de objeto do InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="e6865-118">Create a Form Template Using the InfoPath 2003 Object Model</span></span>](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)

