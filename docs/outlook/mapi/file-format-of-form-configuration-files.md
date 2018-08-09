---
title: Formato de arquivo dos arquivos de configuração de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 86e4ebd9-6df2-4346-9ce9-580f80a83884
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: def91b4e28e60f6d2e8534f0ed7261777ec0c8e0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766536"
---
# <a name="file-format-of-form-configuration-files"></a><span data-ttu-id="e9a75-103">Formato de arquivo dos arquivos de configuração de formulário</span><span class="sxs-lookup"><span data-stu-id="e9a75-103">File format of form configuration files</span></span>

<span data-ttu-id="e9a75-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e9a75-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e9a75-105">Um arquivo de configuração do formulário é um arquivo formatado criado por desenvolvedores de formulário para definir um formulário.</span><span class="sxs-lookup"><span data-stu-id="e9a75-105">A form configuration file is a formatted file created by form developers to define a form.</span></span>
  
<span data-ttu-id="e9a75-106">Como os arquivos de configuração de formulário são usados por gerentes de formulário para carregar formulários, cada formulário deve ser definido usando um arquivo de configuração do formulário.</span><span class="sxs-lookup"><span data-stu-id="e9a75-106">Because form configuration files are used by form managers to load forms, each form must be defined using a form configuration file.</span></span> <span data-ttu-id="e9a75-107">Arquivos de configuração do formulário devem ter a extensão de nome de arquivo. cfg.</span><span class="sxs-lookup"><span data-stu-id="e9a75-107">Form configuration files must have the .cfg filename extension.</span></span> <span data-ttu-id="e9a75-108">O arquivo segue a sintaxe geral de um arquivo de inicialização do Windows (arquivo. ini).</span><span class="sxs-lookup"><span data-stu-id="e9a75-108">The file follows the general syntax of a Windows initialization file (.ini file).</span></span> 

<span data-ttu-id="e9a75-109">Ele é dividido em seções nomeadas, e cada seção contém uma série de entradas e valores.</span><span class="sxs-lookup"><span data-stu-id="e9a75-109">It is divided into named sections, and each section contains a series of entries and values.</span></span> <span data-ttu-id="e9a75-110">Valores tem um dos seguintes tipos: cadeia de caracteres, cadeia de caracteres exibida, cadeia de caracteres de plataforma, caminho, inteiro ou **GUID**, identificador globalmente exclusivo.</span><span class="sxs-lookup"><span data-stu-id="e9a75-110">Values have one of the following types: string, displayed string, platform string, path, integer, or globally unique identifier, **GUID**.</span></span> <span data-ttu-id="e9a75-111">Arquivos de configuração de formulário podem ser criados com qualquer editor de texto ou o processador de texto que seja capaz de salvar arquivos de texto.</span><span class="sxs-lookup"><span data-stu-id="e9a75-111">Form configuration files can be created with any text editor or word processor that is capable of saving text files.</span></span>
  

