---
title: Criar um arquivo de configuração de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aaf3b33d-ad2d-4ef8-847f-1ab1eaf08706
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 97ecafb2e4159c680fd23607f5ed6f8ea3156de7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333016"
---
# <a name="creating-a-form-configuration-file"></a><span data-ttu-id="ac8da-103">Criar um arquivo de configuração de formulário</span><span class="sxs-lookup"><span data-stu-id="ac8da-103">Creating a Form Configuration File</span></span>

  
  
<span data-ttu-id="ac8da-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac8da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac8da-105">Um arquivo de configuração de formulário fornece informações sobre um formulário tanto para o gerente de formulários como usado como para aplicativos clientes.</span><span class="sxs-lookup"><span data-stu-id="ac8da-105">A form configuration file provides information about a form both to the form manager being used and to client applications.</span></span> <span data-ttu-id="ac8da-106">Um arquivo de configuração de formulário contém uma ampla especificação para um formulário, incluindo as propriedades publicadas pelo formulário para uso por clientes de mensagens, os verbos implementados pelo formulário e as plataformas suportadas pelo formulário.</span><span class="sxs-lookup"><span data-stu-id="ac8da-106">A form configuration file contains an extensive specification for a form, including the properties published by the form for use by messaging clients, the verbs implemented by the form, and the platforms supported by the form.</span></span>
  
<span data-ttu-id="ac8da-107">Um arquivo de configuração de formulário é um arquivo com uma extensão. cfg e tem um formato semelhante a um arquivo de inicialização do Windows.</span><span class="sxs-lookup"><span data-stu-id="ac8da-107">A form configuration file is a file with a .cfg extension, and has a format similar to a Windows initialization file.</span></span> <span data-ttu-id="ac8da-108">É um arquivo de texto sem formatação com várias seções.</span><span class="sxs-lookup"><span data-stu-id="ac8da-108">It is a plain text file with a number of sections.</span></span> <span data-ttu-id="ac8da-109">Cada seção começa com um nome de seção, entre colchetes.</span><span class="sxs-lookup"><span data-stu-id="ac8da-109">Each section begins with a section name, enclosed in square brackets.</span></span> <span data-ttu-id="ac8da-110">Cada seção contém uma ou mais linhas que definem valores e configurações relevantes para essa seção.</span><span class="sxs-lookup"><span data-stu-id="ac8da-110">Each section contains one or more lines that define values and settings relevant to that section.</span></span> <span data-ttu-id="ac8da-111">Os valores têm um dos seguintes tipos:</span><span class="sxs-lookup"><span data-stu-id="ac8da-111">Values have one of the following types:</span></span>
  
- <span data-ttu-id="ac8da-112">String</span><span class="sxs-lookup"><span data-stu-id="ac8da-112">String</span></span>
    
- <span data-ttu-id="ac8da-113">Cadeia de caracteres exibida</span><span class="sxs-lookup"><span data-stu-id="ac8da-113">Displayed string</span></span>
    
- <span data-ttu-id="ac8da-114">Cadeia de caracteres de plataforma</span><span class="sxs-lookup"><span data-stu-id="ac8da-114">Platform string</span></span>
    
- <span data-ttu-id="ac8da-115">Nome do caminho</span><span class="sxs-lookup"><span data-stu-id="ac8da-115">Path name</span></span>
    
- <span data-ttu-id="ac8da-116">Inteiro</span><span class="sxs-lookup"><span data-stu-id="ac8da-116">Integer</span></span>
    
- <span data-ttu-id="ac8da-117">GUID</span><span class="sxs-lookup"><span data-stu-id="ac8da-117">GUID</span></span>
    
<span data-ttu-id="ac8da-118">Para obter mais informações sobre as seções de um arquivo. cfg, consulte [formato de arquivo dos arquivos de configuração de formulário](file-format-of-form-configuration-files.md).</span><span class="sxs-lookup"><span data-stu-id="ac8da-118">For more information about the sections of a .cfg file, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ac8da-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac8da-119">See also</span></span>



[<span data-ttu-id="ac8da-120">Desenvolver servidores de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="ac8da-120">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

