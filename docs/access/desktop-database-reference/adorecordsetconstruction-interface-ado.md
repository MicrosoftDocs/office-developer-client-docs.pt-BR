---
title: Interface ADORecordsetConstruction (ADO)
TOCTitle: ADORecordsetConstruction Interface (ADO)
ms:assetid: 2b53aa6e-3b6f-a996-3967-534215fd586c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249060(v=office.15)
ms:contentKeyID: 48543926
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0b99fcfe4fadc3dddf5937ba1043875de43e88d6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464276"
---
# <a name="adorecordsetconstruction-interface-ado"></a><span data-ttu-id="5862b-102">Interface ADORecordsetConstruction (ADO)</span><span class="sxs-lookup"><span data-stu-id="5862b-102">ADORecordsetConstruction Interface (ADO)</span></span>


<span data-ttu-id="5862b-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5862b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5862b-104">A interface **ADORecordsetConstruction** é utilizada para construir um objeto **Recordset** do ADO a partir de um objeto **Rowset** do banco de dados OLE em um aplicativo C/C++.</span><span class="sxs-lookup"><span data-stu-id="5862b-104">The **ADORecordsetConstruction** interface is used to construct an ADO **Recordset** object from an OLE DB **Rowset** object in a C/C++ application.</span></span>

<span data-ttu-id="5862b-105">Essa interface suporta as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="5862b-105">This interface supports the following properties:</span></span>

## <a name="properties"></a><span data-ttu-id="5862b-106">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5862b-106">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5862b-107"><a href="chapter-property-ado.md">Capítulo</a></span><span class="sxs-lookup"><span data-stu-id="5862b-107"><a href="chapter-property-ado.md">Chapter</a></span></span></p></td>
<td><p><span data-ttu-id="5862b-108">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5862b-108">Read/Write.</span></span><br />
<span data-ttu-id="5862b-109">Obtém/define um objeto de banco de dados OLE <strong>capítulo</strong> de/neste objeto <strong>Recordset</strong> do ADO.</span><span class="sxs-lookup"><span data-stu-id="5862b-109">Gets/sets an OLE DB <strong>Chapter</strong> object from/on this ADO <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5862b-110"><a href="rowposition-property-ado.md">RowPosition</a></span><span class="sxs-lookup"><span data-stu-id="5862b-110"><a href="rowposition-property-ado.md">RowPosition</a></span></span></p></td>
<td><p><span data-ttu-id="5862b-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5862b-111">Read/Write.</span></span><br />
<span data-ttu-id="5862b-112">Obtém/define um objeto <strong>RowPosition</strong> do OLE DB a partir de/neste objeto <strong>Recordset</strong> do ADO.</span><span class="sxs-lookup"><span data-stu-id="5862b-112">Gets/sets an OLE DB <strong>RowPosition</strong> object from/on this ADO <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5862b-113"><a href="rowset-property-ado.md">Conjunto de linhas</a></span><span class="sxs-lookup"><span data-stu-id="5862b-113"><a href="rowset-property-ado.md">Rowset</a></span></span></p></td>
<td><p><span data-ttu-id="5862b-114">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5862b-114">Read/Write.</span></span><br />
<span data-ttu-id="5862b-115">Obtém/define um objeto <strong>Rowset</strong> do OLE DB a partir de/neste objeto <strong>Recordset</strong> do ADO.</span><span class="sxs-lookup"><span data-stu-id="5862b-115">Gets/sets an OLE DB <strong>Rowset</strong> object from/on this ADO <strong>Recordset</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a><span data-ttu-id="5862b-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="5862b-116">Methods</span></span>

<span data-ttu-id="5862b-117">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="5862b-117">None.</span></span>

## <a name="events"></a><span data-ttu-id="5862b-118">Eventos</span><span class="sxs-lookup"><span data-stu-id="5862b-118">Events</span></span>

<span data-ttu-id="5862b-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="5862b-119">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="5862b-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="5862b-120">Remarks</span></span>

<span data-ttu-id="5862b-121">Dado um objeto **Rowset** do OLE DB (pRowset), a construção de um objeto do **Recordset** do ADO (), a construção de um **Recordset** do ADO as quantidades de objeto (adoRs) às três operações básicas a seguir:</span><span class="sxs-lookup"><span data-stu-id="5862b-121">Given an OLE DB **Rowset** object (pRowset ), the construction of an ADO **Recordset** object (), the construction of an ADO **Recordset** object (adoRs ) amounts to the following three basic operations:</span></span>

1. <span data-ttu-id="5862b-122">Criar um objeto **Recordset** do ADO:</span><span class="sxs-lookup"><span data-stu-id="5862b-122">Create an ADO **Recordset** object:</span></span>
    
   ```vb
    Recordset20Ptr adoRs;
    adoRs.CreateInstance(__uuidof(Recordset));
   ```
2. <span data-ttu-id="5862b-123">Consultar a interface **IADORecordsetConstruction** no objeto **Recordset**:</span><span class="sxs-lookup"><span data-stu-id="5862b-123">Query the **IADORecordsetConstruction** interface on the **Recordset** object:</span></span>

   ```vb    
    adoRecordsetConstructionPtr adoRsConstruct=NULL;
    adoRs->QueryInterface(__uuidof(ADORecordsetConstruction),
         (void**)&adoRsConstruct);
   ```

3. <span data-ttu-id="5862b-124">Chamar o IADORecordsetConstruction::put\_Rowset o método de propriedade para definir o objeto Rowset do OLE DB no objeto Recordset do ADO:</span><span class="sxs-lookup"><span data-stu-id="5862b-124">Call the IADORecordsetConstruction::put\_Rowset property method to set the OLE DB Rowset object on the ADO Recordset object:</span></span>

   ```vb     
    IUnknown *pUnk=NULL;
    pRowset->QueryInterface(IID_IUnknown, (void**)&pUnk);
    adoRsConstruct->put_Rowset(pUnk);
   ```
<span data-ttu-id="5862b-125">O objeto resultante agora representa o objeto **Recordset** do ADO construído a partir do objeto **Rowset** do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="5862b-125">The resultant object now represents the ADO **Recordset** object constructed from the OLE DB **Rowset** object.</span></span>

<span data-ttu-id="5862b-126">Também é possível construir um objeto **Recordset** do ADO a partir de um objeto **Chapter** ou **RowPosition** do banco de dados OLE.</span><span class="sxs-lookup"><span data-stu-id="5862b-126">You can also construct an ADO **Recordset** object from an OLE DB **Chapter** or **RowPosition** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="5862b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5862b-127">Requirements</span></span>

- <span data-ttu-id="5862b-128">**Versão:** ADO 2.0 e posterior</span><span class="sxs-lookup"><span data-stu-id="5862b-128">**Version:** ADO 2.0 and later</span></span>

- <span data-ttu-id="5862b-129">**Biblioteca:** msado15.dll</span><span class="sxs-lookup"><span data-stu-id="5862b-129">**Library:** msado15.dll</span></span>

- <span data-ttu-id="5862b-130">**UUID:** 00000283-0000-0010-8000-00AA006D2EA4</span><span class="sxs-lookup"><span data-stu-id="5862b-130">**UUID:** 00000283-0000-0010-8000-00AA006D2EA4</span></span>

