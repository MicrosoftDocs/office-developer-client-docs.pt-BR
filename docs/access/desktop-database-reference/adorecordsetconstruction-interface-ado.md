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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281630"
---
# <a name="adorecordsetconstruction-interface-ado"></a><span data-ttu-id="39156-102">Interface ADORecordsetConstruction (ADO)</span><span class="sxs-lookup"><span data-stu-id="39156-102">ADORecordsetConstruction interface (ADO)</span></span>


<span data-ttu-id="39156-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="39156-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="39156-104">A interface **ADORecordsetConstruction** é utilizada para construir um objeto **Recordset** do ADO a partir de um objeto **Rowset** do banco de dados OLE em um aplicativo C/C++.</span><span class="sxs-lookup"><span data-stu-id="39156-104">The **ADORecordsetConstruction** interface is used to construct an ADO **Recordset** object from an OLE DB **Rowset** object in a C/C++ application.</span></span>

<span data-ttu-id="39156-105">Essa interface suporta as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="39156-105">This interface supports the following properties:</span></span>

## <a name="properties"></a><span data-ttu-id="39156-106">Propriedades</span><span class="sxs-lookup"><span data-stu-id="39156-106">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39156-107"><a href="chapter-property-ado.md">Capítulo</a></span><span class="sxs-lookup"><span data-stu-id="39156-107"><a href="chapter-property-ado.md">Chapter</a></span></span></p></td>
<td><p><span data-ttu-id="39156-108">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="39156-108">Read/Write.</span></span><br />
<span data-ttu-id="39156-109">
Obtém/define um objeto <strong>Chapter</strong> do banco de dados OLE desse/nesse objeto <strong>Recordset</strong> do ADO.</span><span class="sxs-lookup"><span data-stu-id="39156-109">Gets/sets an OLE DB <strong>Chapter</strong> object from/on this ADO <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39156-110"><a href="rowposition-property-ado.md">RowPosition</a></span><span class="sxs-lookup"><span data-stu-id="39156-110"><a href="rowposition-property-ado.md">RowPosition</a></span></span></p></td>
<td><p><span data-ttu-id="39156-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="39156-111">Read/Write.</span></span><br />
<span data-ttu-id="39156-112">
Obtém/define um objeto <strong>RowPosition</strong> do banco de dados OLE desse/nesse objeto <strong>Recordset</strong> do ADO.</span><span class="sxs-lookup"><span data-stu-id="39156-112">Gets/sets an OLE DB <strong>RowPosition</strong> object from/on this ADO <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39156-113"><a href="rowset-property-ado.md">Rowset</a></span><span class="sxs-lookup"><span data-stu-id="39156-113"><a href="rowset-property-ado.md">Rowset</a></span></span></p></td>
<td><p><span data-ttu-id="39156-114">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="39156-114">Read/Write.</span></span><br />
<span data-ttu-id="39156-115">
Obtém/define um objeto <strong>Rowset</strong> do banco de dados OLE desse/nesse objeto <strong>Recordset</strong> do ADO.</span><span class="sxs-lookup"><span data-stu-id="39156-115">Gets/sets an OLE DB <strong>Rowset</strong> object from/on this ADO <strong>Recordset</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a><span data-ttu-id="39156-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="39156-116">Methods</span></span>

<span data-ttu-id="39156-117">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="39156-117">None.</span></span>

## <a name="events"></a><span data-ttu-id="39156-118">Eventos</span><span class="sxs-lookup"><span data-stu-id="39156-118">Events</span></span>

<span data-ttu-id="39156-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="39156-119">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="39156-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="39156-120">Remarks</span></span>

<span data-ttu-id="39156-121">Dado um objeto **Rowset** do OLE DB (pRowset ), a construção de um objeto **Recordset** do ADO (), a construção de um objeto **Recordset** do ADO (adoRs ) equivale às três operações básicas a seguir:</span><span class="sxs-lookup"><span data-stu-id="39156-121">Given an OLE DB **Rowset** object (pRowset ), the construction of an ADO **Recordset** object (), the construction of an ADO **Recordset** object (adoRs ) amounts to the following three basic operations:</span></span>

1. <span data-ttu-id="39156-122">Criar um objeto **Recordset** do ADO:</span><span class="sxs-lookup"><span data-stu-id="39156-122">Create an ADO **Recordset** object:</span></span>
    
   ```vb
    Recordset20Ptr adoRs;
    adoRs.CreateInstance(__uuidof(Recordset));
   ```
2. <span data-ttu-id="39156-123">Consultar a interface **IADORecordsetConstruction** no objeto **Recordset**:</span><span class="sxs-lookup"><span data-stu-id="39156-123">Query the **IADORecordsetConstruction** interface on the **Recordset** object:</span></span>

   ```vb    
    adoRecordsetConstructionPtr adoRsConstruct=NULL;
    adoRs->QueryInterface(__uuidof(ADORecordsetConstruction),
         (void**)&adoRsConstruct);
   ```

3. <span data-ttu-id="39156-124">Chame o método da propriedade IADORecordsetConstruction::p ut Rowset para definir o objeto Rowset OLE DB no objeto \_ Recordset do ADO:</span><span class="sxs-lookup"><span data-stu-id="39156-124">Call the IADORecordsetConstruction::put\_Rowset property method to set the OLE DB Rowset object on the ADO Recordset object:</span></span>

   ```vb     
    IUnknown *pUnk=NULL;
    pRowset->QueryInterface(IID_IUnknown, (void**)&pUnk);
    adoRsConstruct->put_Rowset(pUnk);
   ```
<span data-ttu-id="39156-125">O objeto resultante agora representa o objeto **Recordset do** ADO construído a partir do objeto **Rowset** do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="39156-125">The resultant object now represents the ADO **Recordset** object constructed from the OLE DB **Rowset** object.</span></span>

<span data-ttu-id="39156-126">Também é possível construir um objeto **Recordset** do ADO a partir de um objeto **Chapter** ou **RowPosition** do banco de dados OLE.</span><span class="sxs-lookup"><span data-stu-id="39156-126">You can also construct an ADO **Recordset** object from an OLE DB **Chapter** or **RowPosition** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="39156-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39156-127">Requirements</span></span>

- <span data-ttu-id="39156-128">**Versão:** ADO 2.0 e posterior</span><span class="sxs-lookup"><span data-stu-id="39156-128">**Version:** ADO 2.0 and later</span></span>

- <span data-ttu-id="39156-129">**Biblioteca:** msado15.dll</span><span class="sxs-lookup"><span data-stu-id="39156-129">**Library:** msado15.dll</span></span>

- <span data-ttu-id="39156-130">**UUID:** 00000283-0000-0010-8000-00AA006D2EA4</span><span class="sxs-lookup"><span data-stu-id="39156-130">**UUID:** 00000283-0000-0010-8000-00AA006D2EA4</span></span>

