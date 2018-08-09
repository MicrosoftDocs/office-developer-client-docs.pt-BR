---
title: Exemplo de provedor de catálogo de endereços
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ccf1643-5604-4fee-92cc-3d6af00e7f98
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c32017598407760d5dbbb01ee6c28267bbffd152
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766131"
---
# <a name="address-book-provider-sample"></a><span data-ttu-id="5a638-103">Exemplo de provedor de catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="5a638-103">Address Book Provider Sample</span></span>

  
  
<span data-ttu-id="5a638-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5a638-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5a638-105">Esta amostra oferece suporte a um único contêiner somente leitura para nomes para exibição e endereços de email, o qual serão lidas a partir de um arquivo binário plano.</span><span class="sxs-lookup"><span data-stu-id="5a638-105">This sample supports a single read-only container for display names and email addresses, which are read from a flat binary file.</span></span> <span data-ttu-id="5a638-106">O exemplo suporta modelos únicos e todas as opções de configuração, exceto o Assistente de perfil.</span><span class="sxs-lookup"><span data-stu-id="5a638-106">The sample supports one-off templates and all configuration options except the Profile Wizard.</span></span>
  
<span data-ttu-id="5a638-107">Você pode baixar esse exemplo de [Amostras de código do Outlook Messaging API (MAPI)](http://go.microsoft.com/fwlink/?LinkId=129740
).</span><span class="sxs-lookup"><span data-stu-id="5a638-107">You can download this sample from [Outlook Messaging API (MAPI) Code Samples](http://go.microsoft.com/fwlink/?LinkId=129740
).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5a638-108">Executável:</span><span class="sxs-lookup"><span data-stu-id="5a638-108">Executable:</span></span>  <br/> |<span data-ttu-id="5a638-109">SABP32.dll</span><span class="sxs-lookup"><span data-stu-id="5a638-109">SABP32.dll</span></span>  <br/> |
| <span data-ttu-id="5a638-110">Diretório de origem do código:</span><span class="sxs-lookup"><span data-stu-id="5a638-110">Source code directory:</span></span>  <br/> |<span data-ttu-id="5a638-111">SampleAddressBookProvider\SABP</span><span class="sxs-lookup"><span data-stu-id="5a638-111">SampleAddressBookProvider\SABP</span></span>  <br/> |
|<span data-ttu-id="5a638-112">Idioma:</span><span class="sxs-lookup"><span data-stu-id="5a638-112">Language:</span></span>  <br/> |<span data-ttu-id="5a638-113">C++</span><span class="sxs-lookup"><span data-stu-id="5a638-113">C++</span></span>  <br/> |
|<span data-ttu-id="5a638-114">Plataformas:</span><span class="sxs-lookup"><span data-stu-id="5a638-114">Platforms:</span></span>  <br/> |<span data-ttu-id="5a638-115">Microsoft Visual Studio 2008 para compilar para Windows Vista, Windows Server 2008, Windows XP SP2 e Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="5a638-115">Microsoft Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="5a638-116">Recursos compatíveis</span><span class="sxs-lookup"><span data-stu-id="5a638-116">Supported Features</span></span>

<span data-ttu-id="5a638-117">Este exemplo aceita os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="5a638-117">This sample supports the following features:</span></span>
  
- <span data-ttu-id="5a638-118">Restrições de tabela.</span><span class="sxs-lookup"><span data-stu-id="5a638-118">Table restrictions.</span></span> <span data-ttu-id="5a638-119">O exemplo implementa a resolução de nome ambígua e de correspondência de prefixo.</span><span class="sxs-lookup"><span data-stu-id="5a638-119">The sample implements prefix-match and ambiguous-name resolution.</span></span> <span data-ttu-id="5a638-120">Ele não implementa o idioma de restrição de MAPI completo e restrições são compatíveis apenas com o nome para exibição.</span><span class="sxs-lookup"><span data-stu-id="5a638-120">It does not implement the full MAPI restriction language, and restrictions are supported only on the display name.</span></span>
    
- <span data-ttu-id="5a638-121">Uma tabela de exibição de detalhes para os usuários de mensagens.</span><span class="sxs-lookup"><span data-stu-id="5a638-121">A details display table for messaging users.</span></span> 
    
- <span data-ttu-id="5a638-122">Endereços únicos.</span><span class="sxs-lookup"><span data-stu-id="5a638-122">One-off addresses.</span></span>
    
- <span data-ttu-id="5a638-123">Uma caixa de diálogo de pesquisa avançada.</span><span class="sxs-lookup"><span data-stu-id="5a638-123">An advanced search dialog box.</span></span>
    
- <span data-ttu-id="5a638-124">Um [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) interface.</span><span class="sxs-lookup"><span data-stu-id="5a638-124">An [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="5a638-125">Esta interface é suportada parcialmente; seus métodos **IMAPIProp** delegados para a interface **IPropData** .</span><span class="sxs-lookup"><span data-stu-id="5a638-125">This interface is partially supported; its **IMAPIProp** methods are delegated to the **IPropData** interface.</span></span> <span data-ttu-id="5a638-126">Para obter mais informações, consulte o [IPropData: IMAPIProp](ipropdataimapiprop.md) interface.</span><span class="sxs-lookup"><span data-stu-id="5a638-126">For more information, see the [IPropData : IMAPIProp](ipropdataimapiprop.md) interface.</span></span> 
    
- <span data-ttu-id="5a638-127">Configuração interativa e programática.</span><span class="sxs-lookup"><span data-stu-id="5a638-127">Interactive and programmatic configuration.</span></span>
    
## <a name="unsupported-features"></a><span data-ttu-id="5a638-128">Recursos sem suporte</span><span class="sxs-lookup"><span data-stu-id="5a638-128">Unsupported Features</span></span>

<span data-ttu-id="5a638-129">Este exemplo não suporta os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="5a638-129">This sample does not support the following features:</span></span>
  
- <span data-ttu-id="5a638-130">Classificando.</span><span class="sxs-lookup"><span data-stu-id="5a638-130">Sorting.</span></span>
    
- <span data-ttu-id="5a638-131">Listas de distribuição.</span><span class="sxs-lookup"><span data-stu-id="5a638-131">Distribution lists.</span></span>
    
- <span data-ttu-id="5a638-132">Criar, excluir e modificar entradas.</span><span class="sxs-lookup"><span data-stu-id="5a638-132">Creating, deleting, and modifying entries.</span></span>
    
- <span data-ttu-id="5a638-133">Propriedades com vários valores.</span><span class="sxs-lookup"><span data-stu-id="5a638-133">Properties with multiple values.</span></span>
    
- <span data-ttu-id="5a638-134">Propriedades nomeadas.</span><span class="sxs-lookup"><span data-stu-id="5a638-134">Named properties.</span></span>
    
- <span data-ttu-id="5a638-135">Fazer a distinção entre os nomes e o sobrenome em nomes de exibição.</span><span class="sxs-lookup"><span data-stu-id="5a638-135">Distinguishing between first and last names in display names.</span></span>
    
 <span data-ttu-id="5a638-136">**Para instalar o provedor de catálogo de endereços de amostra**</span><span class="sxs-lookup"><span data-stu-id="5a638-136">**To install the Sample Address Book Provider**</span></span>
  
1. <span data-ttu-id="5a638-137">Para baixar o provedor de catálogo de endereços de amostra, consulte [Baixando as amostras de MAPI do Outlook](downloading-the-outlook-mapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="5a638-137">To download the Sample Address Book Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="5a638-138">Localize a pasta onde você salvou as amostras de MAPI do Outlook.</span><span class="sxs-lookup"><span data-stu-id="5a638-138">Locate the folder where you saved the Outlook MAPI Samples.</span></span> <span data-ttu-id="5a638-139">Com o botão direito do **OutlookMAPISamples -\<o número de versão\> ** zip pasta e clique em **Extrair tudo**.</span><span class="sxs-lookup"><span data-stu-id="5a638-139">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and click **Extract All**.</span></span>
    
3. <span data-ttu-id="5a638-140">Clique em **Procurar**, selecione o local onde deseja salvar a amostra e clique em **extrair**.</span><span class="sxs-lookup"><span data-stu-id="5a638-140">Click **Browse**, select the location where you want to save the sample, and click **Extract**.</span></span>
    
4. <span data-ttu-id="5a638-141">Execute o Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="5a638-141">Run Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="5a638-142">No Visual Studio 2008, clique em **arquivo**, selecione **Abrir**e, em seguida, clique em **Project/Solution**.</span><span class="sxs-lookup"><span data-stu-id="5a638-142">In Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="5a638-143">Navegue até o local onde você salvou a amostra, clique em **SABP.vcproj**e, em seguida, clique em **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="5a638-143">Browse to the location where you saved the sample, click **SABP.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="5a638-144">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="5a638-144">On the **Build** menu, click **Build Solution**.</span></span>
    
8. <span data-ttu-id="5a638-145">Na caixa de diálogo **Salvar arquivo como** , clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="5a638-145">In the **Save File As** dialog box, click **Save**.</span></span>
    
9. <span data-ttu-id="5a638-146">Na pasta onde você salvou a amostra, com o botão direito do arquivo **Install. bat** e clique em **Executar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="5a638-146">In the folder where you saved the sample, right-click the **install.bat** file and click **Run as administrator**.</span></span>
    
10. <span data-ttu-id="5a638-147">Na caixa de diálogo **Controle de conta de usuário** , clique em **continuar**.</span><span class="sxs-lookup"><span data-stu-id="5a638-147">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="5a638-148">**Install. bat** copia o arquivo. dll na pasta de instalação do Microsoft Office padrão, C:\Program Files\Microsoft Office\Office12\.</span><span class="sxs-lookup"><span data-stu-id="5a638-148">**Install.bat** copies the .dll to the default Microsoft Office installation folder, C:\Program Files\Microsoft Office\Office12\.</span></span> <span data-ttu-id="5a638-149">Se você tiver instalado os produtos do Office em um local diferente, clique com o botão **Install. bat** e clique em **Editar**.</span><span class="sxs-lookup"><span data-stu-id="5a638-149">If you have installed Office products in a different location, right-click **Install.bat** and click **Edit**.</span></span> <span data-ttu-id="5a638-150">O arquivo será aberto no bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="5a638-150">The file opens in Notepad.</span></span> <span data-ttu-id="5a638-151">Substitua o caminho de instalação padrão do caminho de instalação usado no seu computador.</span><span class="sxs-lookup"><span data-stu-id="5a638-151">Replace the default installation path with the installation path used on your computer.</span></span> 
  

