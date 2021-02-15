---
title: Método CreateObject (RDS)
TOCTitle: CreateObject method (RDS)
ms:assetid: 130debe5-31cf-4ab0-5f78-9adaec7d7126
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248905(v=office.15)
ms:contentKeyID: 48543360
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 47ad61495bcc96b3099af6273796626e9442cbf0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295370"
---
# <a name="createobject-method-rds"></a>Método CreateObject (RDS)

**Aplica-se ao:** Access 2013, Office 2013

Cria o proxy para o objeto corporativo de destino e retorna um ponteiro para ele. O proxy empacota e conduz dados para o stub no servidor para comunicação com o objeto corporativo a fim de enviar solicitações e dados pela Internet. Para objetos de componente dentro do processo, nenhum proxy é utilizado, apenas é fornecido um ponteiro para o objeto.

## <a name="syntax"></a>Sintaxe

O Remote Data Service suporta os seguintes protocolos: HTTP, HTTPS (HTTP sobre Secure Socket Layer), DCOM e dentro do processo.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Protocolo</p></th>
<th><p>Sintaxe</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>HTTP</p></td>
<td><p>Set<em>object</em>  =  <em>DataSpace</em>. CreateObject( &quot; <em>ProgId</em> &quot; , &quot; <em>https://awebsrvr</em> &quot; )</p></td>
</tr>
<tr class="even">
<td><p>HTTPS</p></td>
<td><p>Set<em>object</em>  =  <em>DataSpace</em>. CreateObject( &quot; <em>ProgId</em> &quot; , &quot; <em>https://awebsrvr</em> &quot; )</p></td>
</tr>
<tr class="odd">
<td><p>DCOM</p></td>
<td><p>Set<em>object</em>  =  <em>DataSpace</em>. CreateObject( &quot; <em>ProgId</em> &quot; , &quot; <em>computername</em> &quot; )</p></td>
</tr>
<tr class="even">
<td><p>No processo</p></td>
<td><p>Set<em>object</em>  =  <em>DataSpace</em>. CreateObject( &quot; <em>ProgId</em> &quot; , &quot; &quot; )</p></td>
</tr>
</tbody>
</table>


## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Object* |Uma variável de objeto que é avaliada para um objeto que é o tipo especificado em *ProgID*.|
|*DataSpace* |Uma variável de objeto que representa um objeto [RDS.DataSpace](dataspace-object-rds.md) utilizado para criar uma instância do novo objeto.|
|*ProgID* |Um valor **String** que contém o identificador programático que especifica um objeto corporativo no servidor que implementa as regras comerciais de seu aplicativo.|
|*awebsrvr* ou *computername* |Um **valor String** que representa uma URL que identifica o servidor Web do IIS (Serviços de Informações da Internet) onde uma instância do objeto de negócios do servidor é criada.|

## <a name="remarks"></a>Comentários

O *protocolo HTTP é* o protocolo padrão da Web; *HTTPS* é um protocolo seguro da Web. Utilize o *protocolo DCOM* ao executar uma rede local sem HTTP. O protocolo *dentro do processo* é uma biblioteca de vínculo dinâmico (DLL) local; ele não utiliza uma rede.

