---
title: Interface ADORecordsetConstruction (ADO)
TOCTitle: ADORecordsetConstruction interface (ADO)
ms:assetid: 2b53aa6e-3b6f-a996-3967-534215fd586c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249060(v=office.15)
ms:contentKeyID: 48543926
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 98342d5456c545e6da8539c11f616c08fd52a932
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701270"
---
# <a name="adorecordsetconstruction-interface-ado"></a><span data-ttu-id="01208-102">Interface ADORecordsetConstruction (ADO)</span><span class="sxs-lookup"><span data-stu-id="01208-102">ADORecordsetConstruction interface (ADO)</span></span>


<span data-ttu-id="01208-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="01208-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="01208-104">A interface **ADORecordsetConstruction** é utilizada para construir um objeto **Recordset** do ADO a partir de um objeto **Rowset** do banco de dados OLE em um aplicativo C/C++.</span><span class="sxs-lookup"><span data-stu-id="01208-104">The **ADORecordsetConstruction** interface is used to construct an ADO **Recordset** object from an OLE DB **Rowset** object in a C/C++ application.</span></span>

<span data-ttu-id="01208-105">Essa interface suporta as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="01208-105">This interface supports the following properties:</span></span>

## <a name="properties"></a><span data-ttu-id="01208-106">Propriedades</span><span class="sxs-lookup"><span data-stu-id="01208-106">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="01208-107"><a href="chapter-property-ado.md">Capítulo</a></span><span class="sxs-lookup"><span data-stu-id="01208-107"><a href="chapter-property-ado.md">Chapter</a></span></span></p></td>
<td><p><span data-ttu-id="01208-108">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="01208-108">Read/Write.</span></span><br />
<span data-ttu-id="01208-109">Obtém/define um objeto de banco de dados OLE <strong>capítulo</strong> de/neste objeto <strong>Recordset</strong> do ADO.</span><span class="sxs-lookup"><span data-stu-id="01208-109">Gets/sets an OLE DB <strong>Chapter</strong> object from/on this ADO <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01208-110"><a href="rowposition-property-ado.md">RowPosition</a></span><span class="sxs-lookup"><span data-stu-id="01208-110"><a href="rowposition-property-ado.md">RowPosition</a></span></span></p></td>
<td><p><span data-ttu-id="01208-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="01208-111">Read/Write.</span></span><br />
<span data-ttu-id="01208-112">Obtém/define um objeto <strong>RowPosition</strong> do OLE DB a partir de/neste objeto <strong>Recordset</strong> do ADO.</span><span class="sxs-lookup"><span data-stu-id="01208-112">Gets/sets an OLE DB <strong>RowPosition</strong> object from/on this ADO <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01208-113"><a href="rowset-property-ado.md">Conjunto de linhas</a></span><span class="sxs-lookup"><span data-stu-id="01208-113"><a href="rowset-property-ado.md">Rowset</a></span></span></p></td>
<td><p><span data-ttu-id="01208-114">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="01208-114">Read/Write.</span></span><br />
<span data-ttu-id="01208-115">Obtém/define um objeto <strong>Rowset</strong> do OLE DB a partir de/neste objeto <strong>Recordset</strong> do ADO.</span><span class="sxs-lookup"><span data-stu-id="01208-115">Gets/sets an OLE DB <strong>Rowset</strong> object from/on this ADO <strong>Recordset</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a><span data-ttu-id="01208-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="01208-116">Methods</span></span>

<span data-ttu-id="01208-117">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="01208-117">None.</span></span>

## <a name="events"></a><span data-ttu-id="01208-118">Eventos</span><span class="sxs-lookup"><span data-stu-id="01208-118">Events</span></span>

<span data-ttu-id="01208-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="01208-119">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="01208-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="01208-120">Remarks</span></span>

<span data-ttu-id="01208-121">Dado um objeto **Rowset** do OLE DB (pRowset), a construção de um objeto do **Recordset** do ADO (), a construção de um **Recordset** do ADO as quantidades de objeto (adoRs) às três operações básicas a seguir:</span><span class="sxs-lookup"><span data-stu-id="01208-121">Given an OLE DB **Rowset** object (pRowset ), the construction of an ADO **Recordset** object (), the construction of an ADO **Recordset** object (adoRs ) amounts to the following three basic operations:</span></span>

1. <span data-ttu-id="01208-122">Criar um objeto **Recordset** do ADO:</span><span class="sxs-lookup"><span data-stu-id="01208-122">Create an ADO **Recordset** object:</span></span>
    
   ```vb
    Recordset20Ptr adoRs;
    adoRs.CreateInstance(__uuidof(Recordset));
   ```
2. <span data-ttu-id="01208-123">Consultar a interface **IADORecordsetConstruction** no objeto **Recordset**:</span><span class="sxs-lookup"><span data-stu-id="01208-123">Query the **IADORecordsetConstruction** interface on the **Recordset** object:</span></span>

   ```vb    
    adoRecordsetConstructionPtr adoRsConstruct=NULL;
    adoRs->QueryInterface(__uuidof(ADORecordsetConstruction),
         (void**)&adoRsConstruct);
   ```

3. <span data-ttu-id="01208-124">Chamar o IADORecordsetConstruction::put\_Rowset o método de propriedade para definir o objeto Rowset do OLE DB no objeto Recordset do ADO:</span><span class="sxs-lookup"><span data-stu-id="01208-124">Call the IADORecordsetConstruction::put\_Rowset property method to set the OLE DB Rowset object on the ADO Recordset object:</span></span>

   ```vb     
    IUnknown *pUnk=NULL;
    pRowset->QueryInterface(IID_IUnknown, (void**)&pUnk);
    adoRsConstruct->put_Rowset(pUnk);
   ```
<span data-ttu-id="01208-125">O objeto resultante agora representa o objeto **Recordset** do ADO construído a partir do objeto **Rowset** do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="01208-125">The resultant object now represents the ADO **Recordset** object constructed from the OLE DB **Rowset** object.</span></span>

<span data-ttu-id="01208-126">Também é possível construir um objeto **Recordset** do ADO a partir de um objeto **Chapter** ou **RowPosition** do banco de dados OLE.</span><span class="sxs-lookup"><span data-stu-id="01208-126">You can also construct an ADO **Recordset** object from an OLE DB **Chapter** or **RowPosition** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="01208-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01208-127">Requirements</span></span>

- <span data-ttu-id="01208-128">**Versão:** ADO 2.0 e posterior</span><span class="sxs-lookup"><span data-stu-id="01208-128">**Version:** ADO 2.0 and later</span></span>

- <span data-ttu-id="01208-129">**Biblioteca:** msado15.dll</span><span class="sxs-lookup"><span data-stu-id="01208-129">**Library:** msado15.dll</span></span>

- <span data-ttu-id="01208-130">**UUID:** 00000283-0000-0010-8000-00AA006D2EA4</span><span class="sxs-lookup"><span data-stu-id="01208-130">**UUID:** 00000283-0000-0010-8000-00AA006D2EA4</span></span>

