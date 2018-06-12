---
title: Seção de [plataformas] do arquivo de configuração de formulário
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3b9b3dc0-4f82-468b-8e77-0374c5b196f4
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: ddc6db2303d9d5f114fdb27b6e15e699a04e73f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766591"
---
# <a name="form-configuration-file-platforms-section"></a><span data-ttu-id="22f79-103">Seção de [plataformas] do arquivo de configuração de formulário</span><span class="sxs-lookup"><span data-stu-id="22f79-103">Form Configuration File [Platforms] Section</span></span>

<span data-ttu-id="22f79-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="22f79-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="22f79-105">A seção **[plataformas]** lista o conjunto completo de plataformas suportadas por este formulário.</span><span class="sxs-lookup"><span data-stu-id="22f79-105">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="22f79-106">Cada entrada de plataforma consiste o prefixo **plataforma.**</span><span class="sxs-lookup"><span data-stu-id="22f79-106">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="22f79-107">_cadeia de caracteres_, onde a _cadeia de caracteres_ é um código de cadeia de caracteres arbitrária para a plataforma.</span><span class="sxs-lookup"><span data-stu-id="22f79-107">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="22f79-108">Cada sequência corresponde à entrada de **CPU** de um seções **[plataformas]** individuais.</span><span class="sxs-lookup"><span data-stu-id="22f79-108">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="22f79-109">Cada entrada em uma seção **[plataformas]** define uma _cadeia de caracteres de plataforma_ que faz referência a um subsequentes **[Platform.**</span><span class="sxs-lookup"><span data-stu-id="22f79-109">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="22f79-110">_cadeia de caracteres de plataforma_ seção de **]** , conforme mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="22f79-110">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="22f79-111">A seção **[plataformas]** lista o conjunto completo de plataformas suportadas por este formulário.</span><span class="sxs-lookup"><span data-stu-id="22f79-111">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="22f79-112">Cada entrada de plataforma consiste o prefixo **plataforma.**</span><span class="sxs-lookup"><span data-stu-id="22f79-112">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="22f79-113">_cadeia de caracteres_, onde a _cadeia de caracteres_ é um código de cadeia de caracteres arbitrária para a plataforma.</span><span class="sxs-lookup"><span data-stu-id="22f79-113">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="22f79-114">Cada sequência corresponde à entrada de **CPU** de um seções **[plataformas]** individuais.</span><span class="sxs-lookup"><span data-stu-id="22f79-114">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="22f79-115">Cada entrada em uma seção **[plataformas]** define uma _cadeia de caracteres de plataforma_ que faz referência a um subsequentes **[Platform.**</span><span class="sxs-lookup"><span data-stu-id="22f79-115">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="22f79-116">_cadeia de caracteres de plataforma_ seção de **]** , conforme mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="22f79-116">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="22f79-117">**[Plataformas]**</span><span class="sxs-lookup"><span data-stu-id="22f79-117">**[Platforms]**</span></span>
  
<span data-ttu-id="22f79-118">**Plataforma**.</span><span class="sxs-lookup"><span data-stu-id="22f79-118">**Platform**.</span></span> <span data-ttu-id="22f79-119">_cadeia de caracteres_ =  _cadeia de caracteres de plataforma_</span><span class="sxs-lookup"><span data-stu-id="22f79-119">_string_ =  _platform string_</span></span>
  
<span data-ttu-id="22f79-120">A seguir está um exemplo de uma seção **[plataformas]** .</span><span class="sxs-lookup"><span data-stu-id="22f79-120">Following is an example of a **[Platforms]** section.</span></span> 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

<span data-ttu-id="22f79-121">Cada **[Platform.**</span><span class="sxs-lookup"><span data-stu-id="22f79-121">Each **[Platform.**</span></span> <span data-ttu-id="22f79-122">_cadeia de caracteres de plataforma_ seção de **]** contém as duas entradas necessárias, **CPU** e **OSVersion**.</span><span class="sxs-lookup"><span data-stu-id="22f79-122">_platform string_ **]** section contains the two required entries, **CPU** and **OSVersion**.</span></span> <span data-ttu-id="22f79-123">A entrada de **CPU** Especifica o processador e a entrada de **OSVersion** Especifica o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="22f79-123">The **CPU** entry specifies the processor, and the **OSVersion** entry specifies the operating system.</span></span> <span data-ttu-id="22f79-124">Os valores válidos de **CPU** são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="22f79-124">Valid **CPU** values are described in the following table.</span></span> 
  
|<span data-ttu-id="22f79-125">**Entrada de CPU**</span><span class="sxs-lookup"><span data-stu-id="22f79-125">**CPU Entry**</span></span>|<span data-ttu-id="22f79-126">**Processador**</span><span class="sxs-lookup"><span data-stu-id="22f79-126">**Processor**</span></span>|
|:-----|:-----|
|<span data-ttu-id="22f79-127">Ix86</span><span class="sxs-lookup"><span data-stu-id="22f79-127">Ix86</span></span>  <br/> |<span data-ttu-id="22f79-128">Intel 80 x86 e processadores Pentium da série, bem como processadores de equivalentes da AMD, Cyrix, NextGen e outros fabricantes.</span><span class="sxs-lookup"><span data-stu-id="22f79-128">Intel 80x86 and Pentium series processors, as well as equivalent processors from AMD, Cyrix, NextGen and other manufacturers.</span></span>  <br/> |
|<span data-ttu-id="22f79-129">MIPS</span><span class="sxs-lookup"><span data-stu-id="22f79-129">MIPS</span></span>  <br/> |<span data-ttu-id="22f79-130">Processadores MIPS R4000 da série.</span><span class="sxs-lookup"><span data-stu-id="22f79-130">MIPS R4000 series processors.</span></span>  <br/> |
|<span data-ttu-id="22f79-131">AXP</span><span class="sxs-lookup"><span data-stu-id="22f79-131">AXP</span></span>  <br/> |<span data-ttu-id="22f79-132">Processador de equipamento Corporation Alpha AXP digital.</span><span class="sxs-lookup"><span data-stu-id="22f79-132">Digital Equipment Corporation Alpha AXP processor.</span></span>  <br/> |
|<span data-ttu-id="22f79-133">PPC</span><span class="sxs-lookup"><span data-stu-id="22f79-133">PPC</span></span>  <br/> |<span data-ttu-id="22f79-134">Processadores da série Motorola Power PC.</span><span class="sxs-lookup"><span data-stu-id="22f79-134">Motorola Power PC series processors.</span></span>  <br/> |
|<span data-ttu-id="22f79-135">M68</span><span class="sxs-lookup"><span data-stu-id="22f79-135">M68</span></span>  <br/> |<span data-ttu-id="22f79-136">Processadores Mororola 68 x 00 da série.</span><span class="sxs-lookup"><span data-stu-id="22f79-136">Mororola 68x00 series processors.</span></span>  <br/> |
   
<span data-ttu-id="22f79-137">Os valores válidos de **OSVersion** são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="22f79-137">Valid **OSVersion** values are described in the following table.</span></span> 
  
|<span data-ttu-id="22f79-138">**Entrada de OSVersion**</span><span class="sxs-lookup"><span data-stu-id="22f79-138">**OSVersion Entry**</span></span>|<span data-ttu-id="22f79-139">**Sistema Operacional**</span><span class="sxs-lookup"><span data-stu-id="22f79-139">**Operating System**</span></span>|
|:-----|:-----|
|<span data-ttu-id="22f79-140">Win 3.1</span><span class="sxs-lookup"><span data-stu-id="22f79-140">Win3.1</span></span>  <br/> |<span data-ttu-id="22f79-141">Windows 3.1 e Windows para grupos de trabalho 3.11.</span><span class="sxs-lookup"><span data-stu-id="22f79-141">Windows 3.1 and Windows for Workgroups 3.11.</span></span>  <br/> |
|<span data-ttu-id="22f79-142">WinNT3.5</span><span class="sxs-lookup"><span data-stu-id="22f79-142">WinNT3.5</span></span>  <br/> |<span data-ttu-id="22f79-143">Windows NT 3.5 ou inferior.</span><span class="sxs-lookup"><span data-stu-id="22f79-143">Windows NT 3.5 or lower.</span></span>  <br/> |
|<span data-ttu-id="22f79-144">Win95</span><span class="sxs-lookup"><span data-stu-id="22f79-144">Win95</span></span>  <br/> |<span data-ttu-id="22f79-145">Windows 95.</span><span class="sxs-lookup"><span data-stu-id="22f79-145">Windows 95.</span></span>  <br/> |
|<span data-ttu-id="22f79-146">Winnt 4.0</span><span class="sxs-lookup"><span data-stu-id="22f79-146">WinNT4.0</span></span>  <br/> |<span data-ttu-id="22f79-147">Windows NT 4.0.</span><span class="sxs-lookup"><span data-stu-id="22f79-147">Windows NT 4.0.</span></span>  <br/> |
|<span data-ttu-id="22f79-148">Mac7</span><span class="sxs-lookup"><span data-stu-id="22f79-148">Mac7</span></span>  <br/> |<span data-ttu-id="22f79-149">Sistema 7 para Macintosh.</span><span class="sxs-lookup"><span data-stu-id="22f79-149">Macintosh System 7.</span></span>  <br/> |
   
<span data-ttu-id="22f79-150">Além disso, o **[Platform.**</span><span class="sxs-lookup"><span data-stu-id="22f79-150">Additionally, the **[Platform.**</span></span> <span data-ttu-id="22f79-151">_cadeia de caracteres de plataforma_ seção **]** deve conter uma entrada de um **arquivo** ou o **LinkTo** .</span><span class="sxs-lookup"><span data-stu-id="22f79-151">_platform string_ **]** section must contain either a **File** or **LinkTo** entry.</span></span> <span data-ttu-id="22f79-152">A entrada de **arquivo** lista formulário server arquivo executável do aplicativo que a biblioteca de formulários mantém e carrega em um novo subdiretório no cache de disco quando o formulário for aberto.</span><span class="sxs-lookup"><span data-stu-id="22f79-152">The **File** entry lists the form server application executable file that the form library maintains and loads into a new subdirectory in the disk cache when the form is launched.</span></span> <span data-ttu-id="22f79-153">Se uma entrada de **LinkTo** for usada em vez disso, ele contém o nome de uma cadeia de caracteres de plataforma diferente da qual as informações do **arquivo** são obtidas.</span><span class="sxs-lookup"><span data-stu-id="22f79-153">If a **LinkTo** entry is used instead, it contains the name of a different platform string from which the **File** information is taken.</span></span> <span data-ttu-id="22f79-154">Isso é útil se uma versão de um formulário oferece suporte a várias plataformas.</span><span class="sxs-lookup"><span data-stu-id="22f79-154">This is useful if one version of a form supports multiple platforms.</span></span> 
  
<span data-ttu-id="22f79-155">A entrada **do registro** é utilizada sempre que a entrada de **arquivo** é usada, ele identifica a chave do registro para a biblioteca de formulários, onde o arquivo executável para o aplicativo de servidor do formulário está armazenado.</span><span class="sxs-lookup"><span data-stu-id="22f79-155">The **Registry** entry is used whenever the **File** entry is used, it identifies the registry key for the form library where the executable file for the form server application is stored.</span></span> <span data-ttu-id="22f79-156">As cadeias de caracteres precedidas por uma barra invertida (\) são colocadas na raiz do registro.</span><span class="sxs-lookup"><span data-stu-id="22f79-156">Strings preceded by a backslash ( \ ) are placed at the root of the registry.</span></span> <span data-ttu-id="22f79-157">As cadeias de caracteres não precedidas por uma barra invertida são colocadas na HKEY_CLASSES_ROOT\CLSID\ _GUID_\ chave do registro, onde _GUID_ é o **GUID** do formulário.</span><span class="sxs-lookup"><span data-stu-id="22f79-157">Strings not preceded by a backslash are placed in the HKEY_CLASSES_ROOT\CLSID\  _GUID_\ registry key, where  _GUID_ is the **GUID** of the form.</span></span> <span data-ttu-id="22f79-158">Os caracteres "%d" podem ser usados para indicar o nome do caminho do diretório do qual o arquivo de configuração de formulário foi lido.</span><span class="sxs-lookup"><span data-stu-id="22f79-158">The characters "%d" can be used to indicate the pathname of the directory from which the form configuration file has been read.</span></span> <span data-ttu-id="22f79-159">Isso é útil para especificar outros arquivos com nomes de caminhos em relação ao arquivo de configuração de formulário.</span><span class="sxs-lookup"><span data-stu-id="22f79-159">This is useful for specifying other files with pathnames relative to the form configuration file.</span></span> <span data-ttu-id="22f79-160">Entradas de **Vários arquivos** ou **do registro** podem ser especificadas usando o arquivo ou do registro como um prefixo seguido de qualquer outro texto.</span><span class="sxs-lookup"><span data-stu-id="22f79-160">**Multiple File** or **Registry** entries can be specified by using File or Registry as a prefix followed by any other text.</span></span> <span data-ttu-id="22f79-161">O formato para o **[Platform.**</span><span class="sxs-lookup"><span data-stu-id="22f79-161">The format for the **[Platform.**</span></span> <span data-ttu-id="22f79-162">_cadeia de caracteres de plataforma_ seção **]** é:</span><span class="sxs-lookup"><span data-stu-id="22f79-162">_platform string_ **]** section is:</span></span> 
  
- <span data-ttu-id="22f79-163">**[Platform.**</span><span class="sxs-lookup"><span data-stu-id="22f79-163">**[Platform.**</span></span> <span data-ttu-id="22f79-164">_cadeia de caracteres de plataforma_ **]**</span><span class="sxs-lookup"><span data-stu-id="22f79-164">_platform string_ **]**</span></span>
    
- <span data-ttu-id="22f79-165">**CPU** =  _cadeia de caracteres_</span><span class="sxs-lookup"><span data-stu-id="22f79-165">**CPU** =  _string_</span></span>
    
- <span data-ttu-id="22f79-166">**OSVersion** =  _cadeia de caracteres_</span><span class="sxs-lookup"><span data-stu-id="22f79-166">**OSVersion** =  _string_</span></span>
    
- <span data-ttu-id="22f79-167">**Arquivo** =  _caminho_</span><span class="sxs-lookup"><span data-stu-id="22f79-167">**File** =  _path_</span></span>
    
- <span data-ttu-id="22f79-168">**LinkTo** =  _cadeia de caracteres_</span><span class="sxs-lookup"><span data-stu-id="22f79-168">**LinkTo** =  _string_</span></span>
    
- <span data-ttu-id="22f79-169">**Registro** =  _cadeia de caracteres_</span><span class="sxs-lookup"><span data-stu-id="22f79-169">**Registry** =  _string_</span></span>
  
<span data-ttu-id="22f79-170">A seguir estão dois exemplos **[Platform.**</span><span class="sxs-lookup"><span data-stu-id="22f79-170">The following are two example **[Platform.**</span></span> <span data-ttu-id="22f79-171">_cadeia de caracteres de plataforma_ **]** seções, um usando a entrada de **arquivo** e um usando a entrada **LinkTo** .</span><span class="sxs-lookup"><span data-stu-id="22f79-171">_platform string_ **]** sections, one using the **File** entry and one using the **LinkTo** entry.</span></span> 
  
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

<span data-ttu-id="22f79-172">O **[Platform.**</span><span class="sxs-lookup"><span data-stu-id="22f79-172">The **[Platform.**</span></span> <span data-ttu-id="22f79-173">_cadeia de caracteres de plataforma_ seção **]** é ignorada quando a adição de um formulário para a biblioteca de formulários locais, quando supõe-se que o instalador colocou os arquivos que constitui o manipulador de classe de mensagem no armazenamento local disponível quando nomeados na seção do manipulador no registro do OLE e tiver feito o registro OLE no registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="22f79-173">_platform string_ **]** section is ignored when adding a form to the local form library, when it is assumed that the installer has placed the files constituting the message class handler into available local storage as named in the handler's section in the OLE registry, and has done the OLE registration in the system's registry.</span></span> 
  

