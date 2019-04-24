---
title: Seção do arquivo de configuração de formulários [plataformas]
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3b9b3dc0-4f82-468b-8e77-0374c5b196f4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7439de5b91cefe89eba2f9395595d4a7c8ca3ec5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327507"
---
# <a name="form-configuration-file-platforms-section"></a><span data-ttu-id="f9cfc-103">Seção do arquivo de configuração de formulários [plataformas]</span><span class="sxs-lookup"><span data-stu-id="f9cfc-103">Form Configuration File [Platforms] Section</span></span>

<span data-ttu-id="f9cfc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9cfc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9cfc-105">A seção **[plataformas]** lista o conjunto completo de plataformas suportadas por esse formulário.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-105">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="f9cfc-106">Cada entrada de plataforma consiste na plataforma de prefixo **.**</span><span class="sxs-lookup"><span data-stu-id="f9cfc-106">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="f9cfc-107">_cadeia_de caracteres, onde _cadeia_ de caracteres é um código de cadeia de caracteres arbitrário para a plataforma.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-107">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="f9cfc-108">Cada cadeia de caracteres corresponde à entrada de **CPU** de uma individual **[Platforms]** seções.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-108">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="f9cfc-109">Cada entrada em uma seção **[Platforms]** define uma _cadeia de caracteres de plataforma_ que faz referência a um subseqüente **[Platform.**</span><span class="sxs-lookup"><span data-stu-id="f9cfc-109">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="f9cfc-110">_cadeia de caracteres de plataforma_ **]** como mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-110">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="f9cfc-111">A seção **[plataformas]** lista o conjunto completo de plataformas suportadas por esse formulário.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-111">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="f9cfc-112">Cada entrada de plataforma consiste na plataforma de prefixo **.**</span><span class="sxs-lookup"><span data-stu-id="f9cfc-112">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="f9cfc-113">_cadeia_de caracteres, onde _cadeia_ de caracteres é um código de cadeia de caracteres arbitrário para a plataforma.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-113">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="f9cfc-114">Cada cadeia de caracteres corresponde à entrada de **CPU** de uma individual **[Platforms]** seções.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-114">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="f9cfc-115">Cada entrada em uma seção **[Platforms]** define uma _cadeia de caracteres de plataforma_ que faz referência a um subseqüente **[Platform.**</span><span class="sxs-lookup"><span data-stu-id="f9cfc-115">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="f9cfc-116">_cadeia de caracteres de plataforma_ **]** como mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-116">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="f9cfc-117">**Plataformas**</span><span class="sxs-lookup"><span data-stu-id="f9cfc-117">**[Platforms]**</span></span>
  
<span data-ttu-id="f9cfc-118">**Platform**.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-118">**Platform**.</span></span> <span data-ttu-id="f9cfc-119">__ =  _cadeia_ de caracteres de plataforma de cadeia</span><span class="sxs-lookup"><span data-stu-id="f9cfc-119">_string_ =  _platform string_</span></span>
  
<span data-ttu-id="f9cfc-120">Veja a seguir um exemplo de uma seção **[Platforms]** .</span><span class="sxs-lookup"><span data-stu-id="f9cfc-120">Following is an example of a **[Platforms]** section.</span></span> 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

<span data-ttu-id="f9cfc-121">Cada **[Platform.**</span><span class="sxs-lookup"><span data-stu-id="f9cfc-121">Each **[Platform.**</span></span> <span data-ttu-id="f9cfc-122">_cadeia de caracteres de plataforma_ **]** contém as duas entradas obrigatórias, **CPU** e **OSVersion**.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-122">_platform string_ **]** section contains the two required entries, **CPU** and **OSVersion**.</span></span> <span data-ttu-id="f9cfc-123">A entrada de **CPU** especifica o processador e a entrada **OSVersion** especifica o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-123">The **CPU** entry specifies the processor, and the **OSVersion** entry specifies the operating system.</span></span> <span data-ttu-id="f9cfc-124">Valores de **CPU** válidos são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-124">Valid **CPU** values are described in the following table.</span></span> 
  
|<span data-ttu-id="f9cfc-125">**Entrada de CPU**</span><span class="sxs-lookup"><span data-stu-id="f9cfc-125">**CPU Entry**</span></span>|<span data-ttu-id="f9cfc-126">**Processador**</span><span class="sxs-lookup"><span data-stu-id="f9cfc-126">**Processor**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f9cfc-127">Ix86</span><span class="sxs-lookup"><span data-stu-id="f9cfc-127">Ix86</span></span>  <br/> |<span data-ttu-id="f9cfc-128">Processadores Intel 80x86 e Pentium Series, bem como processadores equivalentes do AMD, Cyrix, NextGen e outros fabricantes.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-128">Intel 80x86 and Pentium series processors, as well as equivalent processors from AMD, Cyrix, NextGen and other manufacturers.</span></span>  <br/> |
|<span data-ttu-id="f9cfc-129">SEQÜENCIA</span><span class="sxs-lookup"><span data-stu-id="f9cfc-129">MIPS</span></span>  <br/> |<span data-ttu-id="f9cfc-130">Processadores da série MIPS R4000.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-130">MIPS R4000 series processors.</span></span>  <br/> |
|<span data-ttu-id="f9cfc-131">AXP</span><span class="sxs-lookup"><span data-stu-id="f9cfc-131">AXP</span></span>  <br/> |<span data-ttu-id="f9cfc-132">Processador Digital Equipment Corporation Alpha AXP.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-132">Digital Equipment Corporation Alpha AXP processor.</span></span>  <br/> |
|<span data-ttu-id="f9cfc-133">PPC</span><span class="sxs-lookup"><span data-stu-id="f9cfc-133">PPC</span></span>  <br/> |<span data-ttu-id="f9cfc-134">Processadores da série Motorola Power PC.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-134">Motorola Power PC series processors.</span></span>  <br/> |
|<span data-ttu-id="f9cfc-135">M68</span><span class="sxs-lookup"><span data-stu-id="f9cfc-135">M68</span></span>  <br/> |<span data-ttu-id="f9cfc-136">Processadores da série mororola 68x00.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-136">Mororola 68x00 series processors.</span></span>  <br/> |
   
<span data-ttu-id="f9cfc-137">Os valores de **OSVersion** válidos são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-137">Valid **OSVersion** values are described in the following table.</span></span> 
  
|<span data-ttu-id="f9cfc-138">**Entrada de OSVersion**</span><span class="sxs-lookup"><span data-stu-id="f9cfc-138">**OSVersion Entry**</span></span>|<span data-ttu-id="f9cfc-139">**Sistema Operacional**</span><span class="sxs-lookup"><span data-stu-id="f9cfc-139">**Operating System**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f9cfc-140">Win 3.1</span><span class="sxs-lookup"><span data-stu-id="f9cfc-140">Win3.1</span></span>  <br/> |<span data-ttu-id="f9cfc-141">Windows 3,1 e Windows para Workgroups 3,11.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-141">Windows 3.1 and Windows for Workgroups 3.11.</span></span>  <br/> |
|<span data-ttu-id="f9cfc-142">WinNT 3.5</span><span class="sxs-lookup"><span data-stu-id="f9cfc-142">WinNT3.5</span></span>  <br/> |<span data-ttu-id="f9cfc-143">Windows NT 3,5 ou inferior.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-143">Windows NT 3.5 or lower.</span></span>  <br/> |
|<span data-ttu-id="f9cfc-144">Win95</span><span class="sxs-lookup"><span data-stu-id="f9cfc-144">Win95</span></span>  <br/> |<span data-ttu-id="f9cfc-145">Windows 95.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-145">Windows 95.</span></span>  <br/> |
|<span data-ttu-id="f9cfc-146">WinNT 4.0</span><span class="sxs-lookup"><span data-stu-id="f9cfc-146">WinNT4.0</span></span>  <br/> |<span data-ttu-id="f9cfc-147">Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-147">Windows NT 4.0.</span></span>  <br/> |
|<span data-ttu-id="f9cfc-148">Mac7</span><span class="sxs-lookup"><span data-stu-id="f9cfc-148">Mac7</span></span>  <br/> |<span data-ttu-id="f9cfc-149">Sistema Macintosh 7.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-149">Macintosh System 7.</span></span>  <br/> |
   
<span data-ttu-id="f9cfc-150">Além disso, o **[Platform.**</span><span class="sxs-lookup"><span data-stu-id="f9cfc-150">Additionally, the **[Platform.**</span></span> <span data-ttu-id="f9cfc-151">_cadeia de caracteres de plataforma_ **]** seção deve conter uma entrada de **arquivo** ou **linkto** .</span><span class="sxs-lookup"><span data-stu-id="f9cfc-151">_platform string_ **]** section must contain either a **File** or **LinkTo** entry.</span></span> <span data-ttu-id="f9cfc-152">A entrada de **arquivo** lista o arquivo executável do aplicativo do servidor de formulário que a biblioteca de formulários mantém e carrega em um novo subdiretório no cache de disco quando o formulário é iniciado.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-152">The **File** entry lists the form server application executable file that the form library maintains and loads into a new subdirectory in the disk cache when the form is launched.</span></span> <span data-ttu-id="f9cfc-153">Se for \*\*\*\* usada uma entrada de linkto, ela conterá o nome de uma cadeia de caracteres de plataforma diferente da qual as informações do **arquivo** foram realizadas.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-153">If a **LinkTo** entry is used instead, it contains the name of a different platform string from which the **File** information is taken.</span></span> <span data-ttu-id="f9cfc-154">Isso será útil se uma versão de um formulário oferecer suporte a várias plataformas.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-154">This is useful if one version of a form supports multiple platforms.</span></span> 
  
<span data-ttu-id="f9cfc-155">A entrada **do registro** é usada sempre que a entrada de **arquivo** é usada, ela identifica a chave do registro para a biblioteca de formulários, onde o arquivo executável do aplicativo do servidor de formulário está armazenado.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-155">The **Registry** entry is used whenever the **File** entry is used, it identifies the registry key for the form library where the executable file for the form server application is stored.</span></span> <span data-ttu-id="f9cfc-156">Cadeias de caracteres precedidas por uma barra invertida (\) são colocadas na raiz do registro.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-156">Strings preceded by a backslash ( \ ) are placed at the root of the registry.</span></span> <span data-ttu-id="f9cfc-157">Cadeias de caracteres não precedidas por uma barra invertida são colocadas na chave HKEY_CLASSES_ROOT\CLSID\ _GUID_\ do registro, onde _GUID_ é o **GUID** do formulário.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-157">Strings not preceded by a backslash are placed in the HKEY_CLASSES_ROOT\CLSID\  _GUID_\ registry key, where  _GUID_ is the **GUID** of the form.</span></span> <span data-ttu-id="f9cfc-158">Os caracteres "% d" podem ser usados para indicar o nome do caminho do diretório a partir do qual o arquivo de configuração de formulário foi lido.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-158">The characters "%d" can be used to indicate the pathname of the directory from which the form configuration file has been read.</span></span> <span data-ttu-id="f9cfc-159">Isso é útil para especificar outros arquivos com Pathnames relativos ao arquivo de configuração de formulário.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-159">This is useful for specifying other files with pathnames relative to the form configuration file.</span></span> <span data-ttu-id="f9cfc-160">**Várias** entradas de arquivo ou **registro** podem ser especificadas usando o arquivo ou registro como um prefixo seguido por qualquer outro texto.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-160">**Multiple File** or **Registry** entries can be specified by using File or Registry as a prefix followed by any other text.</span></span> <span data-ttu-id="f9cfc-161">O formato para o **[Platform.**</span><span class="sxs-lookup"><span data-stu-id="f9cfc-161">The format for the **[Platform.**</span></span> <span data-ttu-id="f9cfc-162">_cadeia de caracteres de plataforma_ **]** seção é:</span><span class="sxs-lookup"><span data-stu-id="f9cfc-162">_platform string_ **]** section is:</span></span> 
  
- <span data-ttu-id="f9cfc-163">**Plataforma.**</span><span class="sxs-lookup"><span data-stu-id="f9cfc-163">**[Platform.**</span></span> <span data-ttu-id="f9cfc-164">_cadeia de caracteres de plataforma_ **]**</span><span class="sxs-lookup"><span data-stu-id="f9cfc-164">_platform string_ **]**</span></span>
    
- <span data-ttu-id="f9cfc-165">\*\*\*\* =  _Cadeia de caracteres_ de CPU</span><span class="sxs-lookup"><span data-stu-id="f9cfc-165">**CPU** =  _string_</span></span>
    
- <span data-ttu-id="f9cfc-166">\*\*\*\* =  _Cadeia de caracteres_ OSVersion</span><span class="sxs-lookup"><span data-stu-id="f9cfc-166">**OSVersion** =  _string_</span></span>
    
- <span data-ttu-id="f9cfc-167">\*\*\*\* =  _Caminho_ do arquivo</span><span class="sxs-lookup"><span data-stu-id="f9cfc-167">**File** =  _path_</span></span>
    
- <span data-ttu-id="f9cfc-168">\*\*\*\* Cadeia de caracteres linkto__  =  </span><span class="sxs-lookup"><span data-stu-id="f9cfc-168">**LinkTo** =  _string_</span></span>
    
- <span data-ttu-id="f9cfc-169">\*\*\*\* =  _Cadeia de caracteres_ do registro</span><span class="sxs-lookup"><span data-stu-id="f9cfc-169">**Registry** =  _string_</span></span>
  
<span data-ttu-id="f9cfc-170">A seguir estão dois exemplos de **[Platform.**</span><span class="sxs-lookup"><span data-stu-id="f9cfc-170">The following are two example **[Platform.**</span></span> <span data-ttu-id="f9cfc-171">_cadeia de caracteres de plataforma_ **]** , uma usando a entrada de **arquivo** e outra usando a entrada **linkto** .</span><span class="sxs-lookup"><span data-stu-id="f9cfc-171">_platform string_ **]** sections, one using the **File** entry and one using the **LinkTo** entry.</span></span> 
  
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

<span data-ttu-id="f9cfc-172">O **[Platform.**</span><span class="sxs-lookup"><span data-stu-id="f9cfc-172">The **[Platform.**</span></span> <span data-ttu-id="f9cfc-173">_cadeia de caracteres de plataforma_ **]** seção é ignorada ao adicionar um formulário à biblioteca de formulários local, quando presume-se que o instalador colocou os arquivos constituting o manipulador de classe de mensagem no armazenamento local disponível como nomeado na seção do manipulador no registro OLE e fez o registro OLE no registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="f9cfc-173">_platform string_ **]** section is ignored when adding a form to the local form library, when it is assumed that the installer has placed the files constituting the message class handler into available local storage as named in the handler's section in the OLE registry, and has done the OLE registration in the system's registry.</span></span> 
  

