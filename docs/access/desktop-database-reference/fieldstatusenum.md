---
title: FieldStatusEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: FieldStatusEnum
ms:assetid: 49570042-8435-8618-3ba1-7006c47735e0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249225(v=office.15)
ms:contentKeyID: 48544635
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 22c5d53427d1380273ea82b3a28ae044e103b179
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860606"
---
# <a name="fieldstatusenum"></a><span data-ttu-id="8e6d1-102">FieldStatusEnum</span><span class="sxs-lookup"><span data-stu-id="8e6d1-102">FieldStatusEnum</span></span>

<span data-ttu-id="8e6d1-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8e6d1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8e6d1-104">Especifica o status de um objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="8e6d1-104">Specifies the status of a **Field** object.</span></span>

<span data-ttu-id="8e6d1-105">O valor **adFieldPending\*** indica a operação que causou a definição do status e pode ser combinado a outros valores de status.</span><span class="sxs-lookup"><span data-stu-id="8e6d1-105">The **adFieldPending\*** values indicate the operation that caused the status to be set, and may be combined with other status values.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8e6d1-106">Constant</span><span class="sxs-lookup"><span data-stu-id="8e6d1-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="8e6d1-107">Valor</span><span class="sxs-lookup"><span data-stu-id="8e6d1-107">Value</span></span></p></th>
<th><p><span data-ttu-id="8e6d1-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e6d1-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8e6d1-109"><strong>adFieldAlreadyExists</strong></span><span class="sxs-lookup"><span data-stu-id="8e6d1-109"><strong>adFieldAlreadyExists</strong></span></span></p></td>
<td><p><span data-ttu-id="8e6d1-110">26</span><span class="sxs-lookup"><span data-stu-id="8e6d1-110">26</span></span></p></td>
<td><p><span data-ttu-id="8e6d1-111">Indica que o campo especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="8e6d1-111">Indicates that the specified field already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e6d1-112"><strong>adFieldBadStatus</strong></span><span class="sxs-lookup"><span data-stu-id="8e6d1-112"><strong>adFieldBadStatus</strong></span></span></p></td>
<td><p><span data-ttu-id="8e6d1-113">12</span><span class="sxs-lookup"><span data-stu-id="8e6d1-113">12</span></span></p></td>
<td><p><span data-ttu-id="8e6d1-p101">Indica que um valor de status inválido foi enviado do ADO para o provedor de OLE DB. As possíveis causas incluem um provedor de OLE DB 1.0 ou 1.1, ou uma combinação inadequada de <a href="value-property-ado.md">Value</a> e <a href="status-property-ado-field.md">Status</a>.</span><span class="sxs-lookup"><span data-stu-id="8e6d1-p101">Indicates that an invalid status value was sent from ADO to the OLE DB provider. Possible causes include an OLE DB 1.0 or 1.1 provider, or an improper combination of <a href="value-property-ado.md">Value</a> and <a href="status-property-ado-field.md">Status</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e6d1-116"><strong>adFieldCannotComplete</strong></span><span class="sxs-lookup"><span data-stu-id="8e6d1-116"><strong>adFieldCannotComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="8e6d1-117">20</span><span class="sxs-lookup"><span data-stu-id="8e6d1-117">20</span></span></p></td>
<td><p><span data-ttu-id="8e6d1-118">Indica que o servidor da URL especificado por <a href="source-property-ado-record.md">Source</a> não pôde concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="8e6d1-118">Indicates that the server of the URL specified by <a href="source-property-ado-record.md">Source</a> could not complete the operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e6d1-119"><strong>adFieldCannotDeleteSource</strong></span><span class="sxs-lookup"><span data-stu-id="8e6d1-119"><strong>adFieldCannotDeleteSource</strong></span></span></p></td>
<td><p><span data-ttu-id="8e6d1-120">23</span><span class="sxs-lookup"><span data-stu-id="8e6d1-120">23</span></span></p></td>
<td><p><span data-ttu-id="8e6d1-121">Indica que durante uma operação move, uma árvore ou subárvore foi movida para uma nova localização, mas a fonte não pôde ser excluída.</span><span class="sxs-lookup"><span data-stu-id="8e6d1-121">Indicates that during a move operation, a tree or subtree was moved to a new location, but the source could not be deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e6d1-122"><strong>adFieldCantConvertValue</strong></span><span class="sxs-lookup"><span data-stu-id="8e6d1-122"><strong>adFieldCantConvertValue</strong></span></span></p></td>
<td><p><span data-ttu-id="8e6d1-123">2</span><span class="sxs-lookup"><span data-stu-id="8e6d1-123">2</span></span></p></td>
<td><p><span data-ttu-id="8e6d1-124">Indica que o campo não pode ser recuperado nem armazenado sem perda de dados.</span><span class="sxs-lookup"><span data-stu-id="8e6d1-124">Indicates that the field cannot be retrieved or stored without loss of data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e6d1-125"><strong>adFieldCantCreate</strong></span><span class="sxs-lookup"><span data-stu-id="8e6d1-125"><strong>adFieldCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="8e6d1-126">7</span><span class="sxs-lookup"><span data-stu-id="8e6d1-126">7</span></span></p></td>
<td><p><span data-ttu-id="8e6d1-127">Indica que o campo não pôde ser adicionado porque o provedor excedeu um limite (como o número permitido de campos).</span><span class="sxs-lookup"><span data-stu-id="8e6d1-127">Indicates that the field could not be added because the provider exceeded a limitation (such as the number of fields allowed).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e6d1-128"><strong>adFieldDataOverflow</strong></span><span class="sxs-lookup"><span data-stu-id="8e6d1-128"><strong>adFieldDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="8e6d1-129">6</span><span class="sxs-lookup"><span data-stu-id="8e6d1-129">6</span></span></p></td>
<td><p><span data-ttu-id="8e6d1-130">Indica que os dados retornados do provedor sobrecarregaram o tipo de dados do campo.</span><span class="sxs-lookup"><span data-stu-id="8e6d1-130">Indicates that the data returned from the provider overflowed the data type of the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e6d1-131"><strong>adFieldDefault</strong></span><span class="sxs-lookup"><span data-stu-id="8e6d1-131"><strong>adFieldDefault</strong></span></span></p></td>
<td><p><span data-ttu-id="8e6d1-132">13</span><span class="sxs-lookup"><span data-stu-id="8e6d1-132">13</span></span></p></td>
<td><p><span data-ttu-id="8e6d1-133">Indica que o valor padrão do campo foi usado durante a definição dos dados.</span><span class="sxs-lookup"><span data-stu-id="8e6d1-133">Indicates that the default value for the field was used when setting data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e6d1-134"><strong>adFieldDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="8e6d1-134"><strong>adFieldDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="8e6d1-135">16</span><span class="sxs-lookup"><span data-stu-id="8e6d1-135">16</span></span></p></td>
<td><p><span data-ttu-id="8e6d1-136">Indica que o campo especificado não existe.</span><span class="sxs-lookup"><span data-stu-id="8e6d1-136">Indicates that the field specified does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e6d1-137"><strong>adFieldIgnore</strong></span><span class="sxs-lookup"><span data-stu-id="8e6d1-137"><strong>adFieldIgnore</strong></span></span></p></td>
<td><p><span data-ttu-id="8e6d1-138">15</span><span class="sxs-lookup"><span data-stu-id="8e6d1-138">15</span></span></p></td>
<td><p><span data-ttu-id="8e6d1-p102">Indica que esse campo foi ignorado quando os valores dos dados foram definidos na fonte. O provedor não definiu nenhum valor.</span><span class="sxs-lookup"><span data-stu-id="8e6d1-p102">Indicates that this field was skipped when setting data values in the source. The provider set no value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e6d1-141"><strong>adFieldIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="8e6d1-141"><strong>adFieldIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="8e6d1-142">10</span><span class="sxs-lookup"><span data-stu-id="8e6d1-142">10</span></span></p></td>
<td><p><span data-ttu-id="8e6d1-143">Indica que não é possível modificar o campo porque ele é uma entidade calculada ou derivada.</span><span class="sxs-lookup"><span data-stu-id="8e6d1-143">Indicates that the field cannot be modified because it is a calculated or derived entity.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e6d1-144"><strong>adFieldInvalidURL</strong></span><span class="sxs-lookup"><span data-stu-id="8e6d1-144"><strong>adFieldInvalidURL</strong></span></span></p></td>
<td><p><span data-ttu-id="8e6d1-145">17</span><span class="sxs-lookup"><span data-stu-id="8e6d1-145">17</span></span></p></td>
<td><p><span data-ttu-id="8e6d1-146">Indica que a URL da fonte de dados contém caracteres inválidos.</span><span class="sxs-lookup"><span data-stu-id="8e6d1-146">Indicates that the data source URL contains invalid characters.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e6d1-147"><strong>adFieldIsNull</strong></span><span class="sxs-lookup"><span data-stu-id="8e6d1-147"><strong>adFieldIsNull</strong></span></span></p></td>
<td><p><span data-ttu-id="8e6d1-148">3</span><span class="sxs-lookup"><span data-stu-id="8e6d1-148">3</span></span></p></td>
<td><p><span data-ttu-id="8e6d1-149">Indica que o provedor retornou um valor VARIANT do tipo VT_NULL e que o campo não está vazio.</span><span class="sxs-lookup"><span data-stu-id="8e6d1-149">Indicates that the provider returned a VARIANT value of type VT_NULL and that the field is not empty.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e6d1-150"><strong>adFieldOK</strong></span><span class="sxs-lookup"><span data-stu-id="8e6d1-150"><strong>adFieldOK</strong></span></span></p></td>
<td><p><span data-ttu-id="8e6d1-151">0</span><span class="sxs-lookup"><span data-stu-id="8e6d1-151">0</span></span></p></td>
<td><p><span data-ttu-id="8e6d1-p103">Padrão. Indica que o campo foi adicionado ou excluído com sucesso.</span><span class="sxs-lookup"><span data-stu-id="8e6d1-p103">Default. Indicates that the field was successfully added or deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e6d1-154"><strong>adFieldOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="8e6d1-154"><strong>adFieldOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="8e6d1-155">22</span><span class="sxs-lookup"><span data-stu-id="8e6d1-155">22</span></span></p></td>
<td><p><span data-ttu-id="8e6d1-156">Indica que o provedor não conseguiu obter espaço de repositório suficiente para concluir uma operação de movimentação ou cópia.</span><span class="sxs-lookup"><span data-stu-id="8e6d1-156">Indicates that the provider is unable to obtain enough storage space to complete a move or copy operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e6d1-157"><strong>adFieldPendingChange</strong></span><span class="sxs-lookup"><span data-stu-id="8e6d1-157"><strong>adFieldPendingChange</strong></span></span></p></td>
<td><p><span data-ttu-id="8e6d1-158">0x40000</span><span class="sxs-lookup"><span data-stu-id="8e6d1-158">0x40000</span></span></p></td>
<td><p><span data-ttu-id="8e6d1-p104">Indica que o campo foi excluído e, em seguida, adicionado novamente, talvez com um tipo de dados diferente, ou que o valor do campo, que anteriormente tinha um status de adFieldOK, foi alterado. O formato final do campo modificará a coleção <a href="fields-collection-ado.md">Fields</a> depois que o método <a href="update-method-ado.md">Update</a> for chamado.</span><span class="sxs-lookup"><span data-stu-id="8e6d1-p104">Indicates either that the field has been deleted and then re-added, perhaps with a different data type, or that the value of the field that previously had a status of adFieldOK has changed. The final form of the field will modify the <a href="fields-collection-ado.md">Fields</a> collection after the <a href="update-method-ado.md">Update</a> method is called.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e6d1-161"><strong>adFieldPendingDelete</strong></span><span class="sxs-lookup"><span data-stu-id="8e6d1-161"><strong>adFieldPendingDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="8e6d1-162">0x20000</span><span class="sxs-lookup"><span data-stu-id="8e6d1-162">0x20000</span></span></p></td>
<td><p><span data-ttu-id="8e6d1-p105">Indica que a operação <strong>Delete</strong> causou a definição do status. O campo foi marcado para ser excluído da coleção <strong>Fields</strong> depois que o método <strong>Update</strong> for chamado.</span><span class="sxs-lookup"><span data-stu-id="8e6d1-p105">Indicates that the <strong>Delete</strong> operation caused the status to be set. The field has been marked for deletion from the <strong>Fields</strong> collection after the <strong>Update</strong> method is called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e6d1-165"><strong>adFieldPendingInsert</strong></span><span class="sxs-lookup"><span data-stu-id="8e6d1-165"><strong>adFieldPendingInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="8e6d1-166">0x10000</span><span class="sxs-lookup"><span data-stu-id="8e6d1-166">0x10000</span></span></p></td>
<td><p><span data-ttu-id="8e6d1-p106">Indica que a operação <strong>Append</strong> causou a definição do status. <strong>Field</strong> foi marcado para ser adicionado à coleção <strong>Fields</strong> depois que o método <strong>Update</strong> for chamado.</span><span class="sxs-lookup"><span data-stu-id="8e6d1-p106">Indicates that the <strong>Append</strong> operation caused the status to be set. The <strong>Field</strong> has been marked to be added to the <strong>Fields</strong> collection after the <strong>Update</strong> method is called.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e6d1-169"><strong>adFieldPendingUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="8e6d1-169"><strong>adFieldPendingUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="8e6d1-170">0x80000</span><span class="sxs-lookup"><span data-stu-id="8e6d1-170">0x80000</span></span></p></td>
<td><p><span data-ttu-id="8e6d1-171">Indica que o provedor não pode determinar quais operações causaram a definição do status do campo.</span><span class="sxs-lookup"><span data-stu-id="8e6d1-171">Indicates that the provider cannot determine what operation caused field status to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e6d1-172"><strong>adFieldPendingUnknownDelete</strong></span><span class="sxs-lookup"><span data-stu-id="8e6d1-172"><strong>adFieldPendingUnknownDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="8e6d1-173">0x100000</span><span class="sxs-lookup"><span data-stu-id="8e6d1-173">0x100000</span></span></p></td>
<td><p><span data-ttu-id="8e6d1-174">Indica que o provedor não pode determinar qual operação causou a definição do status do campo e que o campo será excluído da coleção <strong>Fields</strong> depois que o método <strong>Update</strong> for chamado.</span><span class="sxs-lookup"><span data-stu-id="8e6d1-174">Indicates that the provider cannot determine what operation caused field status to be set, and that the field will be deleted from the <strong>Fields</strong> collection after the <strong>Update</strong> method is called.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e6d1-175"><strong>adFieldPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="8e6d1-175"><strong>adFieldPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="8e6d1-176">9</span><span class="sxs-lookup"><span data-stu-id="8e6d1-176">9</span></span></p></td>
<td><p><span data-ttu-id="8e6d1-177">Indica que o campo não pode ser modificado porque ele está definido como somente-leitura.</span><span class="sxs-lookup"><span data-stu-id="8e6d1-177">Indicates that the field cannot be modified because it is defined as read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e6d1-178"><strong>adFieldReadOnly</strong></span><span class="sxs-lookup"><span data-stu-id="8e6d1-178"><strong>adFieldReadOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="8e6d1-179">24</span><span class="sxs-lookup"><span data-stu-id="8e6d1-179">24</span></span></p></td>
<td><p><span data-ttu-id="8e6d1-180">Indica que o campo na fonte de dados está definido como somente-leitura.</span><span class="sxs-lookup"><span data-stu-id="8e6d1-180">Indicates that the field in the data source is defined as read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e6d1-181"><strong>adFieldResourceExists</strong></span><span class="sxs-lookup"><span data-stu-id="8e6d1-181"><strong>adFieldResourceExists</strong></span></span></p></td>
<td><p><span data-ttu-id="8e6d1-182">19</span><span class="sxs-lookup"><span data-stu-id="8e6d1-182">19</span></span></p></td>
<td><p><span data-ttu-id="8e6d1-183">Indica que o provedor não pôde executar a operação porque um objeto já existe na URL de destino e não é possível sobrescrevê-lo.</span><span class="sxs-lookup"><span data-stu-id="8e6d1-183">Indicates that the provider was unable to perform the operation because an object already exists at the destination URL and it is not able to overwrite the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e6d1-184"><strong>adFieldResourceLocked</strong></span><span class="sxs-lookup"><span data-stu-id="8e6d1-184"><strong>adFieldResourceLocked</strong></span></span></p></td>
<td><p><span data-ttu-id="8e6d1-185">18</span><span class="sxs-lookup"><span data-stu-id="8e6d1-185">18</span></span></p></td>
<td><p><span data-ttu-id="8e6d1-186">Indica que o provedor não pôde executar a operação porque a fonte de dados está bloqueada por um ou mais aplicativos ou processos diferentes.</span><span class="sxs-lookup"><span data-stu-id="8e6d1-186">Indicates that the provider was unable to perform the operation because the data source is locked by one or more other application or process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e6d1-187"><strong>adFieldResourceOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="8e6d1-187"><strong>adFieldResourceOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="8e6d1-188">25</span><span class="sxs-lookup"><span data-stu-id="8e6d1-188">25</span></span></p></td>
<td><p><span data-ttu-id="8e6d1-189">Indica que uma URL de origem ou de destino está fora do escopo do registro atual.</span><span class="sxs-lookup"><span data-stu-id="8e6d1-189">Indicates that a source or destination URL is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e6d1-190"><strong>adFieldSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="8e6d1-190"><strong>adFieldSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="8e6d1-191">11</span><span class="sxs-lookup"><span data-stu-id="8e6d1-191">11</span></span></p></td>
<td><p><span data-ttu-id="8e6d1-192">Indica que o valor violou a restrição do esquema da fonte de dados para o campo.</span><span class="sxs-lookup"><span data-stu-id="8e6d1-192">Indicates that the value violated the data source schema constraint for the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e6d1-193"><strong>adFieldSignMismatch</strong></span><span class="sxs-lookup"><span data-stu-id="8e6d1-193"><strong>adFieldSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="8e6d1-194">5</span><span class="sxs-lookup"><span data-stu-id="8e6d1-194">5</span></span></p></td>
<td><p><span data-ttu-id="8e6d1-195">Indica que o valor dos dados retornado pelo provedor estava assinado, mas o tipo de dados do valor do campo ADO não estava.</span><span class="sxs-lookup"><span data-stu-id="8e6d1-195">Indicates that data value returned by the provider was signed but the data type of the ADO field value was unsigned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e6d1-196"><strong>adFieldTruncated</strong></span><span class="sxs-lookup"><span data-stu-id="8e6d1-196"><strong>adFieldTruncated</strong></span></span></p></td>
<td><p><span data-ttu-id="8e6d1-197">4</span><span class="sxs-lookup"><span data-stu-id="8e6d1-197">4</span></span></p></td>
<td><p><span data-ttu-id="8e6d1-198">Indica que os dados de comprimento variável estavam truncados durante a leitura a partir da fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="8e6d1-198">Indicates that variable-length data was truncated when reading from the data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e6d1-199"><strong>adFieldUnavailable</strong></span><span class="sxs-lookup"><span data-stu-id="8e6d1-199"><strong>adFieldUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="8e6d1-200">8</span><span class="sxs-lookup"><span data-stu-id="8e6d1-200">8</span></span></p></td>
<td><p><span data-ttu-id="8e6d1-p107">Indica que o provedor não pôde determinar o valor durante a leitura da fonte de dados. Por exemplo, a linha acabou de ser criada, o valor padrão para a coluna não está disponível e um novo valor ainda não foi especificado.</span><span class="sxs-lookup"><span data-stu-id="8e6d1-p107">Indicates that the provider could not determine the value when reading from the data source. For example, the row was just created, the default value for the column was not available, and a new value had not yet been specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e6d1-203"><strong>adFieldVolumeNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="8e6d1-203"><strong>adFieldVolumeNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="8e6d1-204">21</span><span class="sxs-lookup"><span data-stu-id="8e6d1-204">21</span></span></p></td>
<td><p><span data-ttu-id="8e6d1-205">Indica que o provedor não pôde localizar o volume de repositório indicado pela URL.</span><span class="sxs-lookup"><span data-stu-id="8e6d1-205">Indicates that the provider is unable to locate the storage volume indicated by the URL.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="8e6d1-206">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="8e6d1-206">ADO/WFC equivalent</span></span>

<span data-ttu-id="8e6d1-207">Essas constantes não têm ADO/WFC equivalentes.</span><span class="sxs-lookup"><span data-stu-id="8e6d1-207">These constants do not have ADO/WFC equivalents.</span></span>

