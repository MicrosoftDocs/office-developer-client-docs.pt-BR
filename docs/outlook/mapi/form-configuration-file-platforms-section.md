---
title: Seção Arquivo de Configuração de Formulário [Plataformas]
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3b9b3dc0-4f82-468b-8e77-0374c5b196f4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7439de5b91cefe89eba2f9395595d4a7c8ca3ec5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419125"
---
# <a name="form-configuration-file-platforms-section"></a><span data-ttu-id="0c980-103">Seção Arquivo de Configuração de Formulário [Plataformas]</span><span class="sxs-lookup"><span data-stu-id="0c980-103">Form Configuration File [Platforms] Section</span></span>

<span data-ttu-id="0c980-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c980-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c980-105">A **seção [Plataformas]** lista o conjunto completo de plataformas com suporte neste formulário.</span><span class="sxs-lookup"><span data-stu-id="0c980-105">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="0c980-106">Cada entrada de plataforma consiste no **prefixo Platform.**</span><span class="sxs-lookup"><span data-stu-id="0c980-106">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="0c980-107">_cadeia_ de caracteres ,  _onde cadeia de_ caracteres é um código de cadeia de caracteres arbitrário para a plataforma.</span><span class="sxs-lookup"><span data-stu-id="0c980-107">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="0c980-108">Cada cadeia de caracteres corresponde à **entrada da CPU** de uma seção **[Plataformas]** individuais.</span><span class="sxs-lookup"><span data-stu-id="0c980-108">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="0c980-109">Cada entrada em uma **seção [Plataformas]** define uma  _cadeia_ de caracteres de plataforma que faz referência a uma **[plataforma] subsequente.**</span><span class="sxs-lookup"><span data-stu-id="0c980-109">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="0c980-110">_cadeia de caracteres_ **de plataforma ]** conforme mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="0c980-110">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="0c980-111">A **seção [Plataformas]** lista o conjunto completo de plataformas com suporte neste formulário.</span><span class="sxs-lookup"><span data-stu-id="0c980-111">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="0c980-112">Cada entrada de plataforma consiste no **prefixo Platform.**</span><span class="sxs-lookup"><span data-stu-id="0c980-112">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="0c980-113">_cadeia_ de caracteres ,  _onde cadeia de_ caracteres é um código de cadeia de caracteres arbitrário para a plataforma.</span><span class="sxs-lookup"><span data-stu-id="0c980-113">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="0c980-114">Cada cadeia de caracteres corresponde à **entrada da CPU** de uma seção **[Plataformas]** individuais.</span><span class="sxs-lookup"><span data-stu-id="0c980-114">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="0c980-115">Cada entrada em uma **seção [Plataformas]** define uma  _cadeia_ de caracteres de plataforma que faz referência a uma **[plataforma] subsequente.**</span><span class="sxs-lookup"><span data-stu-id="0c980-115">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="0c980-116">_cadeia de caracteres_ **de plataforma ]** conforme mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="0c980-116">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="0c980-117">**[Plataformas]**</span><span class="sxs-lookup"><span data-stu-id="0c980-117">**[Platforms]**</span></span>
  
<span data-ttu-id="0c980-118">**Plataforma**.</span><span class="sxs-lookup"><span data-stu-id="0c980-118">**Platform**.</span></span> <span data-ttu-id="0c980-119">_string_  =   _cadeia de caracteres de plataforma_</span><span class="sxs-lookup"><span data-stu-id="0c980-119">_string_ =  _platform string_</span></span>
  
<span data-ttu-id="0c980-120">A seguir está um exemplo de **uma seção [Plataformas].**</span><span class="sxs-lookup"><span data-stu-id="0c980-120">Following is an example of a **[Platforms]** section.</span></span> 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

<span data-ttu-id="0c980-121">Cada **uma [plataforma.**</span><span class="sxs-lookup"><span data-stu-id="0c980-121">Each **[Platform.**</span></span> <span data-ttu-id="0c980-122">_cadeia de caracteres_ de plataforma **]** contém as duas entradas necessárias, **CPU** e **OSVersion**.</span><span class="sxs-lookup"><span data-stu-id="0c980-122">_platform string_ **]** section contains the two required entries, **CPU** and **OSVersion**.</span></span> <span data-ttu-id="0c980-123">A entrada da **CPU** especifica o processador e a **entrada osVersion** especifica o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="0c980-123">The **CPU** entry specifies the processor, and the **OSVersion** entry specifies the operating system.</span></span> <span data-ttu-id="0c980-124">Os **valores válidos** da CPU são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0c980-124">Valid **CPU** values are described in the following table.</span></span> 
  
|<span data-ttu-id="0c980-125">**Entrada da CPU**</span><span class="sxs-lookup"><span data-stu-id="0c980-125">**CPU Entry**</span></span>|<span data-ttu-id="0c980-126">**Processador**</span><span class="sxs-lookup"><span data-stu-id="0c980-126">**Processor**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0c980-127">Ix86</span><span class="sxs-lookup"><span data-stu-id="0c980-127">Ix86</span></span>  <br/> |<span data-ttu-id="0c980-128">Processadores de série Intel 80x86 e Pentium, bem como processadores equivalentes da AMD, Cyila, NextGen e outros fabricantes.</span><span class="sxs-lookup"><span data-stu-id="0c980-128">Intel 80x86 and Pentium series processors, as well as equivalent processors from AMD, Cyrix, NextGen and other manufacturers.</span></span>  <br/> |
|<span data-ttu-id="0c980-129">MIPS</span><span class="sxs-lookup"><span data-stu-id="0c980-129">MIPS</span></span>  <br/> |<span data-ttu-id="0c980-130">Processadores de série MIPS R4000.</span><span class="sxs-lookup"><span data-stu-id="0c980-130">MIPS R4000 series processors.</span></span>  <br/> |
|<span data-ttu-id="0c980-131">AXP</span><span class="sxs-lookup"><span data-stu-id="0c980-131">AXP</span></span>  <br/> |<span data-ttu-id="0c980-132">Processador Digital Equipment Corporation Alpha AXP.</span><span class="sxs-lookup"><span data-stu-id="0c980-132">Digital Equipment Corporation Alpha AXP processor.</span></span>  <br/> |
|<span data-ttu-id="0c980-133">PPC</span><span class="sxs-lookup"><span data-stu-id="0c980-133">PPC</span></span>  <br/> |<span data-ttu-id="0c980-134">Processadores de séries Do Power PC.</span><span class="sxs-lookup"><span data-stu-id="0c980-134">Motorola Power PC series processors.</span></span>  <br/> |
|<span data-ttu-id="0c980-135">M68</span><span class="sxs-lookup"><span data-stu-id="0c980-135">M68</span></span>  <br/> |<span data-ttu-id="0c980-136">Processadores de séries 68x00 Dalmárola.</span><span class="sxs-lookup"><span data-stu-id="0c980-136">Mororola 68x00 series processors.</span></span>  <br/> |
   
<span data-ttu-id="0c980-137">Os **valores válidos** do OSVersion são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0c980-137">Valid **OSVersion** values are described in the following table.</span></span> 
  
|<span data-ttu-id="0c980-138">**Entrada OSVersion**</span><span class="sxs-lookup"><span data-stu-id="0c980-138">**OSVersion Entry**</span></span>|<span data-ttu-id="0c980-139">**Sistema Operacional**</span><span class="sxs-lookup"><span data-stu-id="0c980-139">**Operating System**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0c980-140">Win3.1</span><span class="sxs-lookup"><span data-stu-id="0c980-140">Win3.1</span></span>  <br/> |<span data-ttu-id="0c980-141">Windows 3.1 e Windows for Workgroups 3.11.</span><span class="sxs-lookup"><span data-stu-id="0c980-141">Windows 3.1 and Windows for Workgroups 3.11.</span></span>  <br/> |
|<span data-ttu-id="0c980-142">WinNT3.5</span><span class="sxs-lookup"><span data-stu-id="0c980-142">WinNT3.5</span></span>  <br/> |<span data-ttu-id="0c980-143">Windows NT 3.5 ou inferior.</span><span class="sxs-lookup"><span data-stu-id="0c980-143">Windows NT 3.5 or lower.</span></span>  <br/> |
|<span data-ttu-id="0c980-144">Win95</span><span class="sxs-lookup"><span data-stu-id="0c980-144">Win95</span></span>  <br/> |<span data-ttu-id="0c980-145">Windows 95.</span><span class="sxs-lookup"><span data-stu-id="0c980-145">Windows 95.</span></span>  <br/> |
|<span data-ttu-id="0c980-146">WinNT4.0</span><span class="sxs-lookup"><span data-stu-id="0c980-146">WinNT4.0</span></span>  <br/> |<span data-ttu-id="0c980-147">Windows NT 4.0.</span><span class="sxs-lookup"><span data-stu-id="0c980-147">Windows NT 4.0.</span></span>  <br/> |
|<span data-ttu-id="0c980-148">Mac7</span><span class="sxs-lookup"><span data-stu-id="0c980-148">Mac7</span></span>  <br/> |<span data-ttu-id="0c980-149">Macintosh System 7.</span><span class="sxs-lookup"><span data-stu-id="0c980-149">Macintosh System 7.</span></span>  <br/> |
   
<span data-ttu-id="0c980-150">Além disso, a **[Plataforma.**</span><span class="sxs-lookup"><span data-stu-id="0c980-150">Additionally, the **[Platform.**</span></span> <span data-ttu-id="0c980-151">_cadeia de caracteres_ de plataforma **]** section must contain either a **File** or **LinkTo** entry.</span><span class="sxs-lookup"><span data-stu-id="0c980-151">_platform string_ **]** section must contain either a **File** or **LinkTo** entry.</span></span> <span data-ttu-id="0c980-152">A **entrada Arquivo** lista o arquivo executável do aplicativo do servidor de formulário que a biblioteca de formulário mantém e carrega em um novo subdiretório no cache de disco quando o formulário é lançado.</span><span class="sxs-lookup"><span data-stu-id="0c980-152">The **File** entry lists the form server application executable file that the form library maintains and loads into a new subdirectory in the disk cache when the form is launched.</span></span> <span data-ttu-id="0c980-153">Se uma **entrada LinkTo** for usada, ela conterá o nome de uma cadeia de caracteres de plataforma diferente da qual as informações **de** arquivo são retiradas.</span><span class="sxs-lookup"><span data-stu-id="0c980-153">If a **LinkTo** entry is used instead, it contains the name of a different platform string from which the **File** information is taken.</span></span> <span data-ttu-id="0c980-154">Isso será útil se uma versão de um formulário suportar várias plataformas.</span><span class="sxs-lookup"><span data-stu-id="0c980-154">This is useful if one version of a form supports multiple platforms.</span></span> 
  
<span data-ttu-id="0c980-155">A **entrada do Registro**  é usada sempre que a entrada de arquivo é usada, ela identifica a chave do Registro para a biblioteca de formulário onde o arquivo executável para o aplicativo de servidor de formulário é armazenado.</span><span class="sxs-lookup"><span data-stu-id="0c980-155">The **Registry** entry is used whenever the **File** entry is used, it identifies the registry key for the form library where the executable file for the form server application is stored.</span></span> <span data-ttu-id="0c980-156">As cadeias de caracteres precedidas por uma invertida ( \ ) são colocadas na raiz do registro.</span><span class="sxs-lookup"><span data-stu-id="0c980-156">Strings preceded by a backslash ( \ ) are placed at the root of the registry.</span></span> <span data-ttu-id="0c980-157">Strings not preceded by a backslash are placed in the HKEY_CLASSES_ROOT\CLSID\  _GUID_\ registry key, where  _GUID_ is the **GUID** of the form.</span><span class="sxs-lookup"><span data-stu-id="0c980-157">Strings not preceded by a backslash are placed in the HKEY_CLASSES_ROOT\CLSID\  _GUID_\ registry key, where  _GUID_ is the **GUID** of the form.</span></span> <span data-ttu-id="0c980-158">Os caracteres "%d" podem ser usados para indicar o nome do caminho do diretório do qual o arquivo de configuração de formulário foi lido.</span><span class="sxs-lookup"><span data-stu-id="0c980-158">The characters "%d" can be used to indicate the pathname of the directory from which the form configuration file has been read.</span></span> <span data-ttu-id="0c980-159">Isso é útil para especificar outros arquivos com nomes de caminho relativos ao arquivo de configuração do formulário.</span><span class="sxs-lookup"><span data-stu-id="0c980-159">This is useful for specifying other files with pathnames relative to the form configuration file.</span></span> <span data-ttu-id="0c980-160">**Várias entradas** de **Arquivo** ou registro podem ser especificadas usando Arquivo ou Registro como um prefixo seguido por qualquer outro texto.</span><span class="sxs-lookup"><span data-stu-id="0c980-160">**Multiple File** or **Registry** entries can be specified by using File or Registry as a prefix followed by any other text.</span></span> <span data-ttu-id="0c980-161">O formato para a **[plataforma.**</span><span class="sxs-lookup"><span data-stu-id="0c980-161">The format for the **[Platform.**</span></span> <span data-ttu-id="0c980-162">_cadeia de caracteres_ **de plataforma ]** seção é:</span><span class="sxs-lookup"><span data-stu-id="0c980-162">_platform string_ **]** section is:</span></span> 
  
- <span data-ttu-id="0c980-163">**[Plataforma.**</span><span class="sxs-lookup"><span data-stu-id="0c980-163">**[Platform.**</span></span> <span data-ttu-id="0c980-164">_cadeia de caracteres de_ **plataforma ]**</span><span class="sxs-lookup"><span data-stu-id="0c980-164">_platform string_ **]**</span></span>
    
- <span data-ttu-id="0c980-165">**CPU**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="0c980-165">**CPU** =  _string_</span></span>
    
- <span data-ttu-id="0c980-166">**OSVersion**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="0c980-166">**OSVersion** =  _string_</span></span>
    
- <span data-ttu-id="0c980-167">**Arquivo**  =   _path_</span><span class="sxs-lookup"><span data-stu-id="0c980-167">**File** =  _path_</span></span>
    
- <span data-ttu-id="0c980-168">**LinkTo**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="0c980-168">**LinkTo** =  _string_</span></span>
    
- <span data-ttu-id="0c980-169">**Registro**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="0c980-169">**Registry** =  _string_</span></span>
  
<span data-ttu-id="0c980-170">A seguir estão dois **exemplos [Platform.**</span><span class="sxs-lookup"><span data-stu-id="0c980-170">The following are two example **[Platform.**</span></span> <span data-ttu-id="0c980-171">_cadeia de caracteres_ de plataforma **]** , uma usando a **entrada de** arquivo e outra usando a entrada **LinkTo.**</span><span class="sxs-lookup"><span data-stu-id="0c980-171">_platform string_ **]** sections, one using the **File** entry and one using the **LinkTo** entry.</span></span> 
  
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

<span data-ttu-id="0c980-172">A **[plataforma.**</span><span class="sxs-lookup"><span data-stu-id="0c980-172">The **[Platform.**</span></span> <span data-ttu-id="0c980-173">_cadeia_ de caracteres de plataforma **]** seção é ignorada ao adicionar um formulário à biblioteca de formulário local, quando é assumido que o instalador colocou os arquivos que estão transformando o manipulador de classe de mensagem em armazenamento local disponível conforme nomeado na seção do manipulador no registro OLE e fez o registro OLE no registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="0c980-173">_platform string_ **]** section is ignored when adding a form to the local form library, when it is assumed that the installer has placed the files constituting the message class handler into available local storage as named in the handler's section in the OLE registry, and has done the OLE registration in the system's registry.</span></span> 
  

