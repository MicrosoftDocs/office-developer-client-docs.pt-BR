---
title: Propriedade StayInSync (ADO)
TOCTitle: StayInSync property (ADO)
ms:assetid: 02c95c10-4032-14e1-e506-f334a8787142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248792(v=office.15)
ms:contentKeyID: 48542966
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bdad1155ee759e3b6faa619ebff315cf65afc2b0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872372"
---
# <a name="stayinsync-property-ado"></a><span data-ttu-id="09002-102">Propriedade StayInSync (ADO)</span><span class="sxs-lookup"><span data-stu-id="09002-102">StayInSync property (ADO)</span></span>


<span data-ttu-id="09002-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="09002-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="09002-104">Indica, em um objeto [Recordset](recordset-object-ado.md) hierárquico, se a referência a registros filhos de base (isto é, o *capítulo*) é alterada quando a posição da linha pai é alterada.</span><span class="sxs-lookup"><span data-stu-id="09002-104">Indicates, in a hierarchical [Recordset](recordset-object-ado.md) object, whether the reference to the underlying child records (that is, the *chapter*) changes when the parent row position changes.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="09002-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="09002-105">Settings and return values</span></span>

<span data-ttu-id="09002-p101">Define ou retorna um valor **Boolean**. O valor padrão é **True**. Se for **True**, o capítulo será atualizado se o objeto pai **Recordset** alterar a posição da linha; se for **False**, o capítulo continuará a fazer referência aos dados do capítulo anterior, ainda que o objeto pai **Recordset** tenha alterado a posição da linha.</span><span class="sxs-lookup"><span data-stu-id="09002-p101">Sets or returns a **Boolean** value. The default value is **True**. If **True**, the chapter will be updated if the parent **Recordset** object changes row position; if **False**, the chapter will continue to refer to data in the previous chapter even though the parent **Recordset** object has changed row position.</span></span>

## <a name="remarks"></a><span data-ttu-id="09002-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="09002-109">Remarks</span></span>

<span data-ttu-id="09002-p102">Essa propriedade aplica-se aos Recordsets hierárquicos, como aqueles que contam com suporte do [Microsoft Data Shaping Service para OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), e deve ser definida no **Recordset** pai antes que o **Recordset** filho seja recuperado. Essa propriedade simplifica a navegação pelos conjuntos de registros hierárquicos.</span><span class="sxs-lookup"><span data-stu-id="09002-p102">This property applies to hierarchical Recordsets, such as those supported by the [Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), and must be set on the parent **Recordset** before the child **Recordset** is retrieved. This property simplifies navigating hierarchical recordsets.</span></span>

