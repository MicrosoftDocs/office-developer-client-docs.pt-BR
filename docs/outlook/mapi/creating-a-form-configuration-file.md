---
title: Criar um arquivo de configuração de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aaf3b33d-ad2d-4ef8-847f-1ab1eaf08706
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 9ceb7ad347e73f69eca3463ed2edc4438a45a21f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766352"
---
# <a name="creating-a-form-configuration-file"></a><span data-ttu-id="47419-103">Criar um arquivo de configuração de formulário</span><span class="sxs-lookup"><span data-stu-id="47419-103">Creating a Form Configuration File</span></span>

  
  
<span data-ttu-id="47419-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="47419-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="47419-105">Um arquivo de configuração de formulário fornece informações sobre um formulário para o gerente de formulário que está sendo usada e aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="47419-105">A form configuration file provides information about a form both to the form manager being used and to client applications.</span></span> <span data-ttu-id="47419-106">Um arquivo de configuração do formulário contém uma especificação extensiva para um formulário, incluindo as propriedades publicadas pelo formulário para uso por clientes, os verbos implementados pelo formulário e as plataformas compatíveis com o formulário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="47419-106">A form configuration file contains an extensive specification for a form, including the properties published by the form for use by messaging clients, the verbs implemented by the form, and the platforms supported by the form.</span></span>
  
<span data-ttu-id="47419-107">Um arquivo de configuração do formulário é um arquivo com uma extensão. cfg e tem um formato semelhante a um arquivo de inicialização do Windows.</span><span class="sxs-lookup"><span data-stu-id="47419-107">A form configuration file is a file with a .cfg extension, and has a format similar to a Windows initialization file.</span></span> <span data-ttu-id="47419-108">É um arquivo de texto sem formatação com um número de seções.</span><span class="sxs-lookup"><span data-stu-id="47419-108">It is a plain text file with a number of sections.</span></span> <span data-ttu-id="47419-109">Cada seção começa com um nome de seção, colocado entre colchetes.</span><span class="sxs-lookup"><span data-stu-id="47419-109">Each section begins with a section name, enclosed in square brackets.</span></span> <span data-ttu-id="47419-110">Cada seção contém uma ou mais linhas que definem os valores e configurações relevantes dessa seção.</span><span class="sxs-lookup"><span data-stu-id="47419-110">Each section contains one or more lines that define values and settings relevant to that section.</span></span> <span data-ttu-id="47419-111">Valores tem um dos seguintes tipos:</span><span class="sxs-lookup"><span data-stu-id="47419-111">Values have one of the following types:</span></span>
  
- <span data-ttu-id="47419-112">String</span><span class="sxs-lookup"><span data-stu-id="47419-112">String</span></span>
    
- <span data-ttu-id="47419-113">Cadeia de caracteres exibida</span><span class="sxs-lookup"><span data-stu-id="47419-113">Displayed string</span></span>
    
- <span data-ttu-id="47419-114">Cadeia de caracteres de plataforma</span><span class="sxs-lookup"><span data-stu-id="47419-114">Platform string</span></span>
    
- <span data-ttu-id="47419-115">Nome do caminho</span><span class="sxs-lookup"><span data-stu-id="47419-115">Path name</span></span>
    
- <span data-ttu-id="47419-116">Inteiro</span><span class="sxs-lookup"><span data-stu-id="47419-116">Integer</span></span>
    
- <span data-ttu-id="47419-117">GUID</span><span class="sxs-lookup"><span data-stu-id="47419-117">GUID</span></span>
    
<span data-ttu-id="47419-118">Para obter mais informações sobre as seções de um arquivo. cfg, consulte o [Arquivo de formato do formulário arquivos de configuração](file-format-of-form-configuration-files.md).</span><span class="sxs-lookup"><span data-stu-id="47419-118">For more information about the sections of a .cfg file, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="47419-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="47419-119">See also</span></span>



[<span data-ttu-id="47419-120">Desenvolver servidores de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="47419-120">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

