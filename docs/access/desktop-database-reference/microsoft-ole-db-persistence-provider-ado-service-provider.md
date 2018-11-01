---
title: Microsoft OLE DB Persistence Provider (Provedor de Serviços do ADO)
TOCTitle: Microsoft OLE DB Persistence Provider (ADO Service Provider)
ms:assetid: 22e41769-36eb-5a88-05ed-870938657624
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249007(v=office.15)
ms:contentKeyID: 48543719
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 35cab114da6536ea1a0123e0da2541dd69125824
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877881"
---
# <a name="microsoft-ole-db-persistence-provider-ado-service-provider"></a><span data-ttu-id="c4287-102">Microsoft OLE DB Persistence Provider (Provedor de Serviços do ADO)</span><span class="sxs-lookup"><span data-stu-id="c4287-102">Microsoft OLE DB Persistence Provider (ADO Service Provider)</span></span>


<span data-ttu-id="c4287-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="c4287-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="c4287-p101">O Microsoft OLE DB Persistence Provider permite que você salve um objeto [Recordset](recordset-object-ado.md) em um arquivo e, posteriormente, restaure esse objeto **Recordset** a partir do arquivo. As informações do esquema, os dados e as alterações pendentes são preservados.</span><span class="sxs-lookup"><span data-stu-id="c4287-p101">The Microsoft OLE DB Persistence Provider enables you to save a [Recordset](recordset-object-ado.md) object into a file, and later restore that **Recordset** object from the file. Schema information, data, and pending changes are preserved.</span></span>

<span data-ttu-id="c4287-106">Você pode salvar o objeto **Recordset** usando o formato proprietário ADTG (Advanced Data Table Gram) ou o formato aberto XML (Extensible Markup Language).</span><span class="sxs-lookup"><span data-stu-id="c4287-106">You can save the **Recordset** in either the proprietary Advanced Data Table Gram (ADTG) format, or the open Extensible Markup Language (XML) format.</span></span>

## <a name="provider-keyword"></a><span data-ttu-id="c4287-107">Palavra-chave do provedor</span><span class="sxs-lookup"><span data-stu-id="c4287-107">Provider Keyword</span></span>

<span data-ttu-id="c4287-108">Para invocar esse provedor, especifique na sequência de conexão a palavra-chave e o valor abaixo.</span><span class="sxs-lookup"><span data-stu-id="c4287-108">To invoke this provider, specify the following keyword and value in the connection string.</span></span>

```vb 
 
"Provider=MSPersist" 
```

## <a name="errors"></a><span data-ttu-id="c4287-109">Erros</span><span class="sxs-lookup"><span data-stu-id="c4287-109">Errors</span></span>

<span data-ttu-id="c4287-110">Os seguintes erros emitidos por esse provedor podem ser detectados no seu aplicativo:</span><span class="sxs-lookup"><span data-stu-id="c4287-110">The following errors issued by this provider can be detected in your application.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c4287-111">Constante</span><span class="sxs-lookup"><span data-stu-id="c4287-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="c4287-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="c4287-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c4287-113">E_BADSTREAM</span><span class="sxs-lookup"><span data-stu-id="c4287-113">E_BADSTREAM</span></span></p></td>
<td><p><span data-ttu-id="c4287-114">O arquivo aberto não tem um formato válido (ou seja, o formato não é ADTG ou XML).</span><span class="sxs-lookup"><span data-stu-id="c4287-114">The file opened does not have a valid format (that is, the format is not ADTG or XML).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4287-115">E_CANTPERSISTROWSET</span><span class="sxs-lookup"><span data-stu-id="c4287-115">E_CANTPERSISTROWSET</span></span></p></td>
<td><p><span data-ttu-id="c4287-116">O objeto <strong>Recordset</strong> que foi salvo possui características que impedem o seu armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c4287-116">The <strong>Recordset</strong> object saved has characteristics that prevent it from being stored.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c4287-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="c4287-117">Remarks</span></span>

<span data-ttu-id="c4287-118">O Microsoft OLE DB Persistence Provider não expõe qualquer propriedade dinâmica.</span><span class="sxs-lookup"><span data-stu-id="c4287-118">The Microsoft OLE DB Persistence Provider exposes no dynamic properties.</span></span>

<span data-ttu-id="c4287-119">Atualmente, somente objetos **Recordset** hierárquicos com parâmetros não podem ser salvos.</span><span class="sxs-lookup"><span data-stu-id="c4287-119">Currently, only parameterized hierarchical **Recordset** objects cannot be saved.</span></span>

<span data-ttu-id="c4287-120">Para obter mais informações sobre o armazenamento persistente de objetos **Recordset**, consulte [Persistência de Recordset](more-about-recordset-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="c4287-120">For more information about persistently storing **Recordset** objects, see [Recordset Persistence](more-about-recordset-persistence.md).</span></span>

<span data-ttu-id="c4287-121">Quando um fluxo é usado para abrir um **Recordset**, deve haver sem parâmetros especificado, exceto o parâmetro *Source* do método **Open** .</span><span class="sxs-lookup"><span data-stu-id="c4287-121">When a stream is used to open a **Recordset**, there should be no parameters specified other than the *Source* parameter of the **Open** method.</span></span>

