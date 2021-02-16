---
title: Exemplo de provedor de agenda de endereços
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ccf1643-5604-4fee-92cc-3d6af00e7f98
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fa2a447d0757e75c95d7dc3d9b1dd16b8c7a8084
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331105"
---
# <a name="address-book-provider-sample"></a><span data-ttu-id="e6a07-103">Exemplo de provedor de agenda de endereços</span><span class="sxs-lookup"><span data-stu-id="e6a07-103">Address Book Provider Sample</span></span>

  
  
<span data-ttu-id="e6a07-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6a07-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6a07-105">Este exemplo dá suporte a um único contêiner somente leitura para exibir nomes e endereços de email, que são lidos de um arquivo binário simples.</span><span class="sxs-lookup"><span data-stu-id="e6a07-105">This sample supports a single read-only container for display names and email addresses, which are read from a flat binary file.</span></span> <span data-ttu-id="e6a07-106">O exemplo oferece suporte a modelos one-off e todas as opções de configuração, exceto o Assistente de Perfil.</span><span class="sxs-lookup"><span data-stu-id="e6a07-106">The sample supports one-off templates and all configuration options except the Profile Wizard.</span></span>
  
<span data-ttu-id="e6a07-107">Você pode baixar este exemplo dos exemplos de código [da API de Mensagens do Outlook (MAPI).](https://go.microsoft.com/fwlink/?LinkId=129740
)</span><span class="sxs-lookup"><span data-stu-id="e6a07-107">You can download this sample from [Outlook Messaging API (MAPI) Code Samples](https://go.microsoft.com/fwlink/?LinkId=129740
).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e6a07-108">Executável:</span><span class="sxs-lookup"><span data-stu-id="e6a07-108">Executable:</span></span>  <br/> |<span data-ttu-id="e6a07-109">SABP32.dll</span><span class="sxs-lookup"><span data-stu-id="e6a07-109">SABP32.dll</span></span>  <br/> |
| <span data-ttu-id="e6a07-110">Diretório do código-fonte:</span><span class="sxs-lookup"><span data-stu-id="e6a07-110">Source code directory:</span></span>  <br/> |<span data-ttu-id="e6a07-111">SampleAddressBookProvider\SABP</span><span class="sxs-lookup"><span data-stu-id="e6a07-111">SampleAddressBookProvider\SABP</span></span>  <br/> |
|<span data-ttu-id="e6a07-112">Idioma:</span><span class="sxs-lookup"><span data-stu-id="e6a07-112">Language:</span></span>  <br/> |<span data-ttu-id="e6a07-113">C++</span><span class="sxs-lookup"><span data-stu-id="e6a07-113">C++</span></span>  <br/> |
|<span data-ttu-id="e6a07-114">Plataformas:</span><span class="sxs-lookup"><span data-stu-id="e6a07-114">Platforms:</span></span>  <br/> |<span data-ttu-id="e6a07-115">Microsoft Visual Studio 2008 para compilar para Windows Vista, Windows Server 2008, Windows XP SP2 e Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="e6a07-115">Microsoft Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="e6a07-116">Recursos com suporte</span><span class="sxs-lookup"><span data-stu-id="e6a07-116">Supported Features</span></span>

<span data-ttu-id="e6a07-117">Este exemplo dá suporte aos seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="e6a07-117">This sample supports the following features:</span></span>
  
- <span data-ttu-id="e6a07-118">Restrições de tabela.</span><span class="sxs-lookup"><span data-stu-id="e6a07-118">Table restrictions.</span></span> <span data-ttu-id="e6a07-119">O exemplo implementa a resolução de prefixo e nome ambíguo.</span><span class="sxs-lookup"><span data-stu-id="e6a07-119">The sample implements prefix-match and ambiguous-name resolution.</span></span> <span data-ttu-id="e6a07-120">Ele não implementa a linguagem de restrição MAPI completa e as restrições são suportadas apenas no nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="e6a07-120">It does not implement the full MAPI restriction language, and restrictions are supported only on the display name.</span></span>
    
- <span data-ttu-id="e6a07-121">Uma tabela de exibição de detalhes para usuários de mensagens.</span><span class="sxs-lookup"><span data-stu-id="e6a07-121">A details display table for messaging users.</span></span> 
    
- <span data-ttu-id="e6a07-122">Endereços one-off.</span><span class="sxs-lookup"><span data-stu-id="e6a07-122">One-off addresses.</span></span>
    
- <span data-ttu-id="e6a07-123">Uma caixa de diálogo de pesquisa avançada.</span><span class="sxs-lookup"><span data-stu-id="e6a07-123">An advanced search dialog box.</span></span>
    
- <span data-ttu-id="e6a07-124">Uma [interface IMAPIStatus : IMAPIProp.](imapistatusimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="e6a07-124">An [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="e6a07-125">Essa interface é parcialmente suportada; seus **métodos IMAPIProp** são delegados à interface **IPropData.**</span><span class="sxs-lookup"><span data-stu-id="e6a07-125">This interface is partially supported; its **IMAPIProp** methods are delegated to the **IPropData** interface.</span></span> <span data-ttu-id="e6a07-126">Para obter mais informações, consulte a interface [IPropData : IMAPIProp.](ipropdataimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="e6a07-126">For more information, see the [IPropData : IMAPIProp](ipropdataimapiprop.md) interface.</span></span> 
    
- <span data-ttu-id="e6a07-127">Configuração interativa e programática.</span><span class="sxs-lookup"><span data-stu-id="e6a07-127">Interactive and programmatic configuration.</span></span>
    
## <a name="unsupported-features"></a><span data-ttu-id="e6a07-128">Recursos sem suporte</span><span class="sxs-lookup"><span data-stu-id="e6a07-128">Unsupported Features</span></span>

<span data-ttu-id="e6a07-129">Este exemplo não dá suporte aos seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="e6a07-129">This sample does not support the following features:</span></span>
  
- <span data-ttu-id="e6a07-130">Classificação.</span><span class="sxs-lookup"><span data-stu-id="e6a07-130">Sorting.</span></span>
    
- <span data-ttu-id="e6a07-131">Listas de distribuição.</span><span class="sxs-lookup"><span data-stu-id="e6a07-131">Distribution lists.</span></span>
    
- <span data-ttu-id="e6a07-132">Criação, exclusão e modificação de entradas.</span><span class="sxs-lookup"><span data-stu-id="e6a07-132">Creating, deleting, and modifying entries.</span></span>
    
- <span data-ttu-id="e6a07-133">Propriedades com vários valores.</span><span class="sxs-lookup"><span data-stu-id="e6a07-133">Properties with multiple values.</span></span>
    
- <span data-ttu-id="e6a07-134">Propriedades nomeadas.</span><span class="sxs-lookup"><span data-stu-id="e6a07-134">Named properties.</span></span>
    
- <span data-ttu-id="e6a07-135">Distinção entre o nome e o sobrenome em nomes de exibição.</span><span class="sxs-lookup"><span data-stu-id="e6a07-135">Distinguishing between first and last names in display names.</span></span>
    
 <span data-ttu-id="e6a07-136">**Para instalar o Provedor de Lista de Endereços de Exemplo**</span><span class="sxs-lookup"><span data-stu-id="e6a07-136">**To install the Sample Address Book Provider**</span></span>
  
1. <span data-ttu-id="e6a07-137">Para baixar o Provedor de Livro de Endereços de Exemplo, consulte [Baixando os exemplos de MAPI do Outlook.](downloading-the-outlook-mapi-samples.md)</span><span class="sxs-lookup"><span data-stu-id="e6a07-137">To download the Sample Address Book Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="e6a07-138">Localize a pasta onde você salvou os exemplos de MAPI do Outlook.</span><span class="sxs-lookup"><span data-stu-id="e6a07-138">Locate the folder where you saved the Outlook MAPI Samples.</span></span> <span data-ttu-id="e6a07-139">Clique com o botão direito do mouse na pasta zip do número de versão do **OutlookMAPISamples \< \>** e clique em **Extrair Tudo.**</span><span class="sxs-lookup"><span data-stu-id="e6a07-139">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and click **Extract All**.</span></span>
    
3. <span data-ttu-id="e6a07-140">Clique **em** Procurar, selecione o local onde deseja salvar o exemplo e clique em **Extrair.**</span><span class="sxs-lookup"><span data-stu-id="e6a07-140">Click **Browse**, select the location where you want to save the sample, and click **Extract**.</span></span>
    
4. <span data-ttu-id="e6a07-141">Execute o Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="e6a07-141">Run Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="e6a07-142">No Visual Studio 2008, clique em **Arquivo,** selecione **Abrir** e clique em **Projeto/Solução.**</span><span class="sxs-lookup"><span data-stu-id="e6a07-142">In Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="e6a07-143">Navegue até o local onde você salvou o exemplo, clique **em SABP.vcproj** e, em seguida, clique em **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="e6a07-143">Browse to the location where you saved the sample, click **SABP.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="e6a07-144">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="e6a07-144">On the **Build** menu, click **Build Solution**.</span></span>
    
8. <span data-ttu-id="e6a07-145">Na caixa **de diálogo Salvar Arquivo como,** clique em **Salvar.**</span><span class="sxs-lookup"><span data-stu-id="e6a07-145">In the **Save File As** dialog box, click **Save**.</span></span>
    
9. <span data-ttu-id="e6a07-146">Na pasta onde você salvou o exemplo, clique com o botão direito do mouse no **arquivoinstall.bat** e clique em **Executar como administrador.**</span><span class="sxs-lookup"><span data-stu-id="e6a07-146">In the folder where you saved the sample, right-click the **install.bat** file and click **Run as administrator**.</span></span>
    
10. <span data-ttu-id="e6a07-147">Na caixa de diálogo **Controle de Conta de Usuário**, clique em **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="e6a07-147">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="e6a07-148">**Install.bat** copia a .dll para a pasta de instalação padrão do Microsoft Office, C:\Arquivos de Programas\Microsoft Office\Office12\.</span><span class="sxs-lookup"><span data-stu-id="e6a07-148">**Install.bat** copies the .dll to the default Microsoft Office installation folder, C:\Program Files\Microsoft Office\Office12\.</span></span> <span data-ttu-id="e6a07-149">Se você instalou produtos do Office em um local diferente, clique com o botão direito do mouse **Install.bat** e clique em **Editar.**</span><span class="sxs-lookup"><span data-stu-id="e6a07-149">If you have installed Office products in a different location, right-click **Install.bat** and click **Edit**.</span></span> <span data-ttu-id="e6a07-150">O arquivo é aberto no Bloco de Notas.</span><span class="sxs-lookup"><span data-stu-id="e6a07-150">The file opens in Notepad.</span></span> <span data-ttu-id="e6a07-151">Substitua o caminho de instalação padrão pelo caminho de instalação usado no computador.</span><span class="sxs-lookup"><span data-stu-id="e6a07-151">Replace the default installation path with the installation path used on your computer.</span></span> 
  

