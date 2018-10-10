---
title: Interface ADORecordConstruction (ADO)
TOCTitle: ADORecordConstruction Interface (ADO)
ms:assetid: 3f0afbdb-f1c4-e44e-7c0f-a0c4cee554a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249175(v=office.15)
ms:contentKeyID: 48544387
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 44272067d8018836fd7eb3d6cfaa762780f69868
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463677"
---
# <a name="adorecordconstruction-interface-ado"></a><span data-ttu-id="d21d3-102">Interface ADORecordConstruction (ADO)</span><span class="sxs-lookup"><span data-stu-id="d21d3-102">ADORecordConstruction Interface (ADO)</span></span>


<span data-ttu-id="d21d3-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d21d3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d21d3-104">A interface **ADORecordConstruction** é utilizada para construir um objeto **Record** do ADO a partir de um objeto **Row** do banco de dados OLE em um aplicativo C/C++.</span><span class="sxs-lookup"><span data-stu-id="d21d3-104">The **ADORecordConstruction** interface is used to construct an ADO **Record** object from an OLE DB **Row** object in a C/C++ application.</span></span>

<span data-ttu-id="d21d3-105">Essa interface suporta as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="d21d3-105">This interface supports the following properties:</span></span>

## <a name="properties"></a><span data-ttu-id="d21d3-106">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d21d3-106">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d21d3-107"><a href="parentrow-property-ado.md">ParentRow</a></span><span class="sxs-lookup"><span data-stu-id="d21d3-107"><a href="parentrow-property-ado.md">ParentRow</a></span></span></p></td>
<td><p><span data-ttu-id="d21d3-108">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="d21d3-108">Write-only.</span></span><br />
<span data-ttu-id="d21d3-109">Define o contêiner de um objeto <strong>Row</strong> do OLE DB neste objeto <strong>Record</strong> do ADO.</span><span class="sxs-lookup"><span data-stu-id="d21d3-109">Sets the container of an OLE DB <strong>Row</strong> object on this ADO <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d21d3-110"><a href="row-property-ado.md">Row</a></span><span class="sxs-lookup"><span data-stu-id="d21d3-110"><a href="row-property-ado.md">Row</a></span></span></p></td>
<td><p><span data-ttu-id="d21d3-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="d21d3-111">Read/Write.</span></span><br />
<span data-ttu-id="d21d3-112">Obtém/define um objeto do OLE DB <strong>linha</strong> a partir de/neste objeto <strong>Record</strong> do ADO.</span><span class="sxs-lookup"><span data-stu-id="d21d3-112">Gets/sets an OLE DB <strong>Row</strong> object from/on this ADO <strong>Record</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a><span data-ttu-id="d21d3-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="d21d3-113">Methods</span></span>

<span data-ttu-id="d21d3-114">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="d21d3-114">None.</span></span>

## <a name="events"></a><span data-ttu-id="d21d3-115">Eventos</span><span class="sxs-lookup"><span data-stu-id="d21d3-115">Events</span></span>

<span data-ttu-id="d21d3-116">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="d21d3-116">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="d21d3-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="d21d3-117">Remarks</span></span>

<span data-ttu-id="d21d3-118">Dado um objeto OLE DB **linha** (pRow), a construção de um objeto de **registro** do ADO (), a construção de um objeto **Record** do ADO (objeto adoR), quantidades às três operações básicas a seguir:</span><span class="sxs-lookup"><span data-stu-id="d21d3-118">Given an OLE DB **Row** object (pRow), the construction of an ADO **Record** object (), the construction of an ADO **Record** object (adoR), amounts to the following three basic operations:</span></span>

1.  <span data-ttu-id="d21d3-119">Criar um objeto **Record** do ADO:</span><span class="sxs-lookup"><span data-stu-id="d21d3-119">Create an ADO **Record** object:</span></span>
    
    ```vb
        _RecordPtr adoR;
        adoRs.CreateInstance(__uuidof(_Record));
    ```

2.  <span data-ttu-id="d21d3-120">Consultar a interface **IADORecordConstruction** no objeto **Record**:</span><span class="sxs-lookup"><span data-stu-id="d21d3-120">Query the **IADORecordConstruction** interface on the **Record** object:</span></span>
    
    ```vb
        adoRecordConstructionPtr adoRConstruct=NULL;
        adoR->QueryInterface(__uuidof(ADORecordConstruction),
                            (void**)&adoRConstruct);
    ```

3.  <span data-ttu-id="d21d3-121">Chamar o **IADORecordConstruction::put\_linha** método de propriedade para definir o objeto OLE DB **linha** no objeto **Record** do ADO:</span><span class="sxs-lookup"><span data-stu-id="d21d3-121">Call the **IADORecordConstruction::put\_Row** property method to set the OLE DB **Row** object on the ADO **Record** object:</span></span>
    
    ```vb
        IUnknown *pUnk=NULL;
        pRow->QueryInterface(IID_IUnknown, (void**)&pUnk);
        adoRConstruct->put_Row(pUnk);
    ```
    
<span data-ttu-id="d21d3-122">O objeto **adoR** resultante agora representa o objeto **Record** do ADO construído a partir do objeto **Row** do banco de dados OLE.</span><span class="sxs-lookup"><span data-stu-id="d21d3-122">The resultant **adoR** object now represents the ADO **Record** object constructed from the OLE DB **Row** object.</span></span>

<span data-ttu-id="d21d3-123">Um objeto **Record** do ADO também pode ser construído a partir do contêiner de um objeto **Row** do banco de dados OLE.</span><span class="sxs-lookup"><span data-stu-id="d21d3-123">An ADO **Record** object can also be constructed from the container of an OLE DB **Row** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="d21d3-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d21d3-124">Requirements</span></span>

<span data-ttu-id="d21d3-125">**Versão:** ADO 2.0 e posterior</span><span class="sxs-lookup"><span data-stu-id="d21d3-125">**Version:** ADO 2.0 and later</span></span>

<span data-ttu-id="d21d3-126">**Biblioteca:** msado15.dll</span><span class="sxs-lookup"><span data-stu-id="d21d3-126">**Library:** msado15.dll</span></span>

<span data-ttu-id="d21d3-127">**UUID:** 00000567-0000-0010-8000-00AA006D2EA4</span><span class="sxs-lookup"><span data-stu-id="d21d3-127">**UUID:** 00000567-0000-0010-8000-00AA006D2EA4</span></span>

