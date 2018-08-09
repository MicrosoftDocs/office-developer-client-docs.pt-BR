---
title: Seção do arquivo de configuração de formulários [Plataformas]
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3b9b3dc0-4f82-468b-8e77-0374c5b196f4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ddc6db2303d9d5f114fdb27b6e15e699a04e73f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766591"
---
# <a name="form-configuration-file-platforms-section"></a><span data-ttu-id="823c0-103">Seção do arquivo de configuração de formulários [Plataformas]</span><span class="sxs-lookup"><span data-stu-id="823c0-103">Form Configuration File [Platforms] Section</span></span>

<span data-ttu-id="823c0-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="823c0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="823c0-105">A seção **[plataformas]** lista o conjunto completo de plataformas suportadas por este formulário.</span><span class="sxs-lookup"><span data-stu-id="823c0-105">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="823c0-106">Cada entrada de plataforma consiste o prefixo **plataforma.**</span><span class="sxs-lookup"><span data-stu-id="823c0-106">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="823c0-107">_cadeia de caracteres_, onde a _cadeia de caracteres_ é um código de cadeia de caracteres arbitrária para a plataforma.</span><span class="sxs-lookup"><span data-stu-id="823c0-107">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="823c0-108">Cada sequência corresponde à entrada de **CPU** de um seções **[plataformas]** individuais.</span><span class="sxs-lookup"><span data-stu-id="823c0-108">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="823c0-109">Cada entrada em uma seção **[plataformas]** define uma _cadeia de caracteres de plataforma_ que faz referência a um subsequentes **[Platform.**</span><span class="sxs-lookup"><span data-stu-id="823c0-109">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="823c0-110">_cadeia de caracteres de plataforma_ seção de **]** , conforme mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="823c0-110">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="823c0-111">A seção **[plataformas]** lista o conjunto completo de plataformas suportadas por este formulário.</span><span class="sxs-lookup"><span data-stu-id="823c0-111">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="823c0-112">Cada entrada de plataforma consiste o prefixo **plataforma.**</span><span class="sxs-lookup"><span data-stu-id="823c0-112">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="823c0-113">_cadeia de caracteres_, onde a _cadeia de caracteres_ é um código de cadeia de caracteres arbitrária para a plataforma.</span><span class="sxs-lookup"><span data-stu-id="823c0-113">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="823c0-114">Cada sequência corresponde à entrada de **CPU** de um seções **[plataformas]** individuais.</span><span class="sxs-lookup"><span data-stu-id="823c0-114">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="823c0-115">Cada entrada em uma seção **[plataformas]** define uma _cadeia de caracteres de plataforma_ que faz referência a um subsequentes **[Platform.**</span><span class="sxs-lookup"><span data-stu-id="823c0-115">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="823c0-116">_cadeia de caracteres de plataforma_ seção de **]** , conforme mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="823c0-116">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="823c0-117">**[Plataformas]**</span><span class="sxs-lookup"><span data-stu-id="823c0-117">**[Platforms]**</span></span>
  
<span data-ttu-id="823c0-118">**Plataforma**.</span><span class="sxs-lookup"><span data-stu-id="823c0-118">**Platform**.</span></span> <span data-ttu-id="823c0-119">_cadeia de caracteres_ =  _cadeia de caracteres de plataforma_</span><span class="sxs-lookup"><span data-stu-id="823c0-119">_string_ =  _platform string_</span></span>
  
<span data-ttu-id="823c0-120">A seguir está um exemplo de uma seção **[plataformas]** .</span><span class="sxs-lookup"><span data-stu-id="823c0-120">Following is an example of a **[Platforms]** section.</span></span> 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

<span data-ttu-id="823c0-121">Cada **[Platform.**</span><span class="sxs-lookup"><span data-stu-id="823c0-121">Each **[Platform.**</span></span> <span data-ttu-id="823c0-122">_cadeia de caracteres de plataforma_ seção de **]** contém as duas entradas necessárias, **CPU** e **OSVersion**.</span><span class="sxs-lookup"><span data-stu-id="823c0-122">_platform string_ **]** section contains the two required entries, **CPU** and **OSVersion**.</span></span> <span data-ttu-id="823c0-123">A entrada de **CPU** Especifica o processador e a entrada de **OSVersion** Especifica o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="823c0-123">The **CPU** entry specifies the processor, and the **OSVersion** entry specifies the operating system.</span></span> <span data-ttu-id="823c0-124">Os valores válidos de **CPU** são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="823c0-124">Valid **CPU** values are described in the following table.</span></span> 
  
|<span data-ttu-id="823c0-125">**Entrada de CPU**</span><span class="sxs-lookup"><span data-stu-id="823c0-125">**CPU Entry**</span></span>|<span data-ttu-id="823c0-126">**Processador**</span><span class="sxs-lookup"><span data-stu-id="823c0-126">**Processor**</span></span>|
|:-----|:-----|
|<span data-ttu-id="823c0-127">Ix86</span><span class="sxs-lookup"><span data-stu-id="823c0-127">Ix86</span></span>  <br/> |<span data-ttu-id="823c0-128">Intel 80 x86 e processadores Pentium da série, bem como processadores de equivalentes da AMD, Cyrix, NextGen e outros fabricantes.</span><span class="sxs-lookup"><span data-stu-id="823c0-128">Intel 80x86 and Pentium series processors, as well as equivalent processors from AMD, Cyrix, NextGen and other manufacturers.</span></span>  <br/> |
|<span data-ttu-id="823c0-129">MIPS</span><span class="sxs-lookup"><span data-stu-id="823c0-129">MIPS</span></span>  <br/> |<span data-ttu-id="823c0-130">Processadores MIPS R4000 da série.</span><span class="sxs-lookup"><span data-stu-id="823c0-130">MIPS R4000 series processors.</span></span>  <br/> |
|<span data-ttu-id="823c0-131">AXP</span><span class="sxs-lookup"><span data-stu-id="823c0-131">AXP</span></span>  <br/> |<span data-ttu-id="823c0-132">Processador de equipamento Corporation Alpha AXP digital.</span><span class="sxs-lookup"><span data-stu-id="823c0-132">Digital Equipment Corporation Alpha AXP processor.</span></span>  <br/> |
|<span data-ttu-id="823c0-133">PPC</span><span class="sxs-lookup"><span data-stu-id="823c0-133">PPC</span></span>  <br/> |<span data-ttu-id="823c0-134">Processadores da série Motorola Power PC.</span><span class="sxs-lookup"><span data-stu-id="823c0-134">Motorola Power PC series processors.</span></span>  <br/> |
|<span data-ttu-id="823c0-135">M68</span><span class="sxs-lookup"><span data-stu-id="823c0-135">M68</span></span>  <br/> |<span data-ttu-id="823c0-136">Processadores Mororola 68 x 00 da série.</span><span class="sxs-lookup"><span data-stu-id="823c0-136">Mororola 68x00 series processors.</span></span>  <br/> |
   
<span data-ttu-id="823c0-137">Os valores válidos de **OSVersion** são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="823c0-137">Valid **OSVersion** values are described in the following table.</span></span> 
  
|<span data-ttu-id="823c0-138">**Entrada de OSVersion**</span><span class="sxs-lookup"><span data-stu-id="823c0-138">**OSVersion Entry**</span></span>|<span data-ttu-id="823c0-139">**Sistema Operacional**</span><span class="sxs-lookup"><span data-stu-id="823c0-139">**Operating System**</span></span>|
|:-----|:-----|
|<span data-ttu-id="823c0-140">Win 3.1</span><span class="sxs-lookup"><span data-stu-id="823c0-140">Win3.1</span></span>  <br/> |<span data-ttu-id="823c0-141">Windows 3.1 e Windows para grupos de trabalho 3.11.</span><span class="sxs-lookup"><span data-stu-id="823c0-141">Windows 3.1 and Windows for Workgroups 3.11.</span></span>  <br/> |
|<span data-ttu-id="823c0-142">WinNT3.5</span><span class="sxs-lookup"><span data-stu-id="823c0-142">WinNT3.5</span></span>  <br/> |<span data-ttu-id="823c0-143">Windows NT 3.5 ou inferior.</span><span class="sxs-lookup"><span data-stu-id="823c0-143">Windows NT 3.5 or lower.</span></span>  <br/> |
|<span data-ttu-id="823c0-144">Win95</span><span class="sxs-lookup"><span data-stu-id="823c0-144">Win95</span></span>  <br/> |<span data-ttu-id="823c0-145">Windows 95.</span><span class="sxs-lookup"><span data-stu-id="823c0-145">Windows 95.</span></span>  <br/> |
|<span data-ttu-id="823c0-146">Winnt 4.0</span><span class="sxs-lookup"><span data-stu-id="823c0-146">WinNT4.0</span></span>  <br/> |<span data-ttu-id="823c0-147">Windows NT 4.0.</span><span class="sxs-lookup"><span data-stu-id="823c0-147">Windows NT 4.0.</span></span>  <br/> |
|<span data-ttu-id="823c0-148">Mac7</span><span class="sxs-lookup"><span data-stu-id="823c0-148">Mac7</span></span>  <br/> |<span data-ttu-id="823c0-149">Sistema 7 para Macintosh.</span><span class="sxs-lookup"><span data-stu-id="823c0-149">Macintosh System 7.</span></span>  <br/> |
   
<span data-ttu-id="823c0-150">Além disso, o **[Platform.**</span><span class="sxs-lookup"><span data-stu-id="823c0-150">Additionally, the **[Platform.**</span></span> <span data-ttu-id="823c0-151">_cadeia de caracteres de plataforma_ seção **]** deve conter uma entrada de um **arquivo** ou o **LinkTo** .</span><span class="sxs-lookup"><span data-stu-id="823c0-151">_platform string_ **]** section must contain either a **File** or **LinkTo** entry.</span></span> <span data-ttu-id="823c0-152">A entrada de **arquivo** lista formulário server arquivo executável do aplicativo que a biblioteca de formulários mantém e carrega em um novo subdiretório no cache de disco quando o formulário for aberto.</span><span class="sxs-lookup"><span data-stu-id="823c0-152">The **File** entry lists the form server application executable file that the form library maintains and loads into a new subdirectory in the disk cache when the form is launched.</span></span> <span data-ttu-id="823c0-153">Se uma entrada de **LinkTo** for usada em vez disso, ele contém o nome de uma cadeia de caracteres de plataforma diferente da qual as informações do **arquivo** são obtidas.</span><span class="sxs-lookup"><span data-stu-id="823c0-153">If a **LinkTo** entry is used instead, it contains the name of a different platform string from which the **File** information is taken.</span></span> <span data-ttu-id="823c0-154">Isso é útil se uma versão de um formulário oferece suporte a várias plataformas.</span><span class="sxs-lookup"><span data-stu-id="823c0-154">This is useful if one version of a form supports multiple platforms.</span></span> 
  
<span data-ttu-id="823c0-155">A entrada **do registro** é utilizada sempre que a entrada de **arquivo** é usada, ele identifica a chave do registro para a biblioteca de formulários, onde o arquivo executável para o aplicativo de servidor do formulário está armazenado.</span><span class="sxs-lookup"><span data-stu-id="823c0-155">The **Registry** entry is used whenever the **File** entry is used, it identifies the registry key for the form library where the executable file for the form server application is stored.</span></span> <span data-ttu-id="823c0-156">As cadeias de caracteres precedidas por uma barra invertida (\) são colocadas na raiz do registro.</span><span class="sxs-lookup"><span data-stu-id="823c0-156">Strings preceded by a backslash ( \ ) are placed at the root of the registry.</span></span> <span data-ttu-id="823c0-157">As cadeias de caracteres não precedidas por uma barra invertida são colocadas na HKEY_CLASSES_ROOT\CLSID\ _GUID_\ chave do registro, onde _GUID_ é o **GUID** do formulário.</span><span class="sxs-lookup"><span data-stu-id="823c0-157">Strings not preceded by a backslash are placed in the HKEY_CLASSES_ROOT\CLSID\  _GUID_\ registry key, where  _GUID_ is the **GUID** of the form.</span></span> <span data-ttu-id="823c0-158">Os caracteres "%d" podem ser usados para indicar o nome do caminho do diretório do qual o arquivo de configuração de formulário foi lido.</span><span class="sxs-lookup"><span data-stu-id="823c0-158">The characters "%d" can be used to indicate the pathname of the directory from which the form configuration file has been read.</span></span> <span data-ttu-id="823c0-159">Isso é útil para especificar outros arquivos com nomes de caminhos em relação ao arquivo de configuração de formulário.</span><span class="sxs-lookup"><span data-stu-id="823c0-159">This is useful for specifying other files with pathnames relative to the form configuration file.</span></span> <span data-ttu-id="823c0-160">Entradas de **Vários arquivos** ou **do registro** podem ser especificadas usando o arquivo ou do registro como um prefixo seguido de qualquer outro texto.</span><span class="sxs-lookup"><span data-stu-id="823c0-160">**Multiple File** or **Registry** entries can be specified by using File or Registry as a prefix followed by any other text.</span></span> <span data-ttu-id="823c0-161">O formato para o **[Platform.**</span><span class="sxs-lookup"><span data-stu-id="823c0-161">The format for the **[Platform.**</span></span> <span data-ttu-id="823c0-162">_cadeia de caracteres de plataforma_ seção **]** é:</span><span class="sxs-lookup"><span data-stu-id="823c0-162">_platform string_ **]** section is:</span></span> 
  
- <span data-ttu-id="823c0-163">**[Platform.**</span><span class="sxs-lookup"><span data-stu-id="823c0-163">**[Platform.**</span></span> <span data-ttu-id="823c0-164">_cadeia de caracteres de plataforma_ **]**</span><span class="sxs-lookup"><span data-stu-id="823c0-164">_platform string_ **]**</span></span>
    
- <span data-ttu-id="823c0-165">**CPU** =  _cadeia de caracteres_</span><span class="sxs-lookup"><span data-stu-id="823c0-165">**CPU** =  _string_</span></span>
    
- <span data-ttu-id="823c0-166">**OSVersion** =  _cadeia de caracteres_</span><span class="sxs-lookup"><span data-stu-id="823c0-166">**OSVersion** =  _string_</span></span>
    
- <span data-ttu-id="823c0-167">**Arquivo** =  _caminho_</span><span class="sxs-lookup"><span data-stu-id="823c0-167">**File** =  _path_</span></span>
    
- <span data-ttu-id="823c0-168">**LinkTo** =  _cadeia de caracteres_</span><span class="sxs-lookup"><span data-stu-id="823c0-168">**LinkTo** =  _string_</span></span>
    
- <span data-ttu-id="823c0-169">**Registro** =  _cadeia de caracteres_</span><span class="sxs-lookup"><span data-stu-id="823c0-169">**Registry** =  _string_</span></span>
  
<span data-ttu-id="823c0-170">A seguir estão dois exemplos **[Platform.**</span><span class="sxs-lookup"><span data-stu-id="823c0-170">The following are two example **[Platform.**</span></span> <span data-ttu-id="823c0-171">_cadeia de caracteres de plataforma_ **]** seções, um usando a entrada de **arquivo** e um usando a entrada **LinkTo** .</span><span class="sxs-lookup"><span data-stu-id="823c0-171">_platform string_ **]** sections, one using the **File** entry and one using the **LinkTo** entry.</span></span> 
  
```cpp
[Platform.NTx86]
CPU = ix86
OSVersion = WinNT3.5
File = \helpdesk.exe
Registry = Local Server = %d\helpdesk.exe
[Platform.Win95]
CPU = ix86
OSVersion = Win95
LinkTo = NTx86

```

<span data-ttu-id="823c0-172">O **[Platform.**</span><span class="sxs-lookup"><span data-stu-id="823c0-172">The **[Platform.**</span></span> <span data-ttu-id="823c0-173">_cadeia de caracteres de plataforma_ seção **]** é ignorada quando a adição de um formulário para a biblioteca de formulários locais, quando supõe-se que o instalador colocou os arquivos que constitui o manipulador de classe de mensagem no armazenamento local disponível quando nomeados na seção do manipulador no registro do OLE e tiver feito o registro OLE no registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="823c0-173">_platform string_ **]** section is ignored when adding a form to the local form library, when it is assumed that the installer has placed the files constituting the message class handler into available local storage as named in the handler's section in the OLE registry, and has done the OLE registration in the system's registry.</span></span> 
  

