---
title: Função OPENFILE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251471
localization_priority: Normal
ms.assetid: ff59ab04-a589-cf9e-db3b-20658a7dffdc
description: Abre um documento do Microsoft Visio, se ainda não estiver aberto, e ativa a janela do documento.
ms.openlocfilehash: 5a89a658e560d144007ec19796de82b9949bea82
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419573"
---
# <a name="openfile-function"></a><span data-ttu-id="1a72e-103">Função OPENFILE</span><span class="sxs-lookup"><span data-stu-id="1a72e-103">OPENFILE Function</span></span>

<span data-ttu-id="1a72e-104">Abre um documento do Microsoft Visio, se ainda não estiver aberto, e ativa a janela do documento.</span><span class="sxs-lookup"><span data-stu-id="1a72e-104">Opens a Microsoft Visio document, if it's not already open, and activates the document window.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="1a72e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a72e-105">Syntax</span></span>

 <span data-ttu-id="1a72e-106">**OPENFILE** ( _"NomeArquivo"_)</span><span class="sxs-lookup"><span data-stu-id="1a72e-106">**OPENFILE**( _"filename"_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="1a72e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a72e-107">Parameters</span></span>

|<span data-ttu-id="1a72e-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="1a72e-108">**Name**</span></span>|<span data-ttu-id="1a72e-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="1a72e-109">**Required/Optional**</span></span>|<span data-ttu-id="1a72e-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="1a72e-110">**Data Type**</span></span>|<span data-ttu-id="1a72e-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1a72e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1a72e-112">_nomes_</span><span class="sxs-lookup"><span data-stu-id="1a72e-112">_filename_</span></span> <br/> |<span data-ttu-id="1a72e-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1a72e-113">Required</span></span>  <br/> |<span data-ttu-id="1a72e-114">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1a72e-114">**String**</span></span> <br/> |<span data-ttu-id="1a72e-115">O nome do arquivo, incluindo o caminho do arquivo, que você deseja abrir.</span><span class="sxs-lookup"><span data-stu-id="1a72e-115">The name of the file, including file path, you want to open.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a72e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a72e-116">Remarks</span></span>

<span data-ttu-id="1a72e-p101">Chamadas múltiplas da função OPENFILE permanecem na fila e são executadas por ordem de avaliação. Se o documento atual do Visio estiver ativo para edição visual (in-loco), uma nova instância do Visio será inicializada com o nome de arquivo solicitado.</span><span class="sxs-lookup"><span data-stu-id="1a72e-p101">Multiple OPENFILE function calls are queued and executed in order of evaluation. If the current Visio document is activated for visual (in-place) editing, a new Visio instance is launched with the requested file name.</span></span> 
  
<span data-ttu-id="1a72e-119">Essa função sempre retornará FALSO.</span><span class="sxs-lookup"><span data-stu-id="1a72e-119">This function always returns FALSE.</span></span> 
  
<span data-ttu-id="1a72e-p102">Em versões anteriores do aplicativo Visio, essa função aparece como _OPENFILE. As versões 4.0 e posteriores do Visio aceitam os dois estilos.</span><span class="sxs-lookup"><span data-stu-id="1a72e-p102">In earlier versions of the Visio application, this function appears as _OPENFILE. Visio versions 4.0 and later accept either style.</span></span> 
  
## <a name="example"></a><span data-ttu-id="1a72e-122">Exemplo</span><span class="sxs-lookup"><span data-stu-id="1a72e-122">Example</span></span>

 `OPENFILE("C:/MyFile.vsdx")`
  
<span data-ttu-id="1a72e-123">Abre o arquivo especificado "MyFile. vsdx" em uma nova janela ou ativa a janela se o arquivo já estiver aberto.</span><span class="sxs-lookup"><span data-stu-id="1a72e-123">Opens the specified file "MyFile.vsdx" in a new window, or activates the window if the file is already open.</span></span> 
  

