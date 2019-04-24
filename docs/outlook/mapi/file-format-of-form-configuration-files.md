---
title: Formato de arquivo dos arquivos de configuração de formulários
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 86e4ebd9-6df2-4346-9ce9-580f80a83884
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d07d88d7b8b892a82832f91989e322ea3b32e040
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334822"
---
# <a name="file-format-of-form-configuration-files"></a><span data-ttu-id="f63f4-103">Formato de arquivo dos arquivos de configuração de formulários</span><span class="sxs-lookup"><span data-stu-id="f63f4-103">File format of form configuration files</span></span>

<span data-ttu-id="f63f4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f63f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f63f4-105">Um arquivo de configuração de formulário é um arquivo formatado criado por desenvolvedores de formulários para definir um formulário.</span><span class="sxs-lookup"><span data-stu-id="f63f4-105">A form configuration file is a formatted file created by form developers to define a form.</span></span>
  
<span data-ttu-id="f63f4-106">Como os arquivos de configuração de formulário são usados por gerentes de formulários para carregar formulários, cada formulário deve ser definido usando um arquivo de configuração de formulário.</span><span class="sxs-lookup"><span data-stu-id="f63f4-106">Because form configuration files are used by form managers to load forms, each form must be defined using a form configuration file.</span></span> <span data-ttu-id="f63f4-107">Arquivos de configuração de formulário devem ter a extensão de nome de arquivo. cfg.</span><span class="sxs-lookup"><span data-stu-id="f63f4-107">Form configuration files must have the .cfg filename extension.</span></span> <span data-ttu-id="f63f4-108">O arquivo segue a sintaxe geral de um arquivo de inicialização do Windows (arquivo. ini).</span><span class="sxs-lookup"><span data-stu-id="f63f4-108">The file follows the general syntax of a Windows initialization file (.ini file).</span></span> 

<span data-ttu-id="f63f4-109">Ele é dividido em seções nomeadas e cada seção contém uma série de entradas e valores.</span><span class="sxs-lookup"><span data-stu-id="f63f4-109">It is divided into named sections, and each section contains a series of entries and values.</span></span> <span data-ttu-id="f63f4-110">Os valores têm um dos seguintes tipos: cadeia de caracteres, Cadeia de caracteres exibida, Cadeia de caracteres de plataforma, caminho, inteiro ou identificador global exclusivo, **GUID**.</span><span class="sxs-lookup"><span data-stu-id="f63f4-110">Values have one of the following types: string, displayed string, platform string, path, integer, or globally unique identifier, **GUID**.</span></span> <span data-ttu-id="f63f4-111">Os arquivos de configuração de formulário podem ser criados com qualquer editor de texto ou processador de textos que possa salvar arquivos de texto.</span><span class="sxs-lookup"><span data-stu-id="f63f4-111">Form configuration files can be created with any text editor or word processor that is capable of saving text files.</span></span>
  

