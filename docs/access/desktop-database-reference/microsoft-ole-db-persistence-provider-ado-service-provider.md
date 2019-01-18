---
title: Microsoft OLE DB Persistence Provider (Provedor de Serviços do ADO)
TOCTitle: Microsoft OLE DB Persistence Provider (ADO Service Provider)
ms:assetid: 22e41769-36eb-5a88-05ed-870938657624
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249007(v=office.15)
ms:contentKeyID: 48543719
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4045445120d42f1ca88fce22ce566fc970fce28b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715505"
---
# <a name="microsoft-ole-db-persistence-provider-ado-service-provider"></a>Microsoft OLE DB Persistence Provider (Provedor de Serviços do ADO)


**Aplica-se a**: Access 2013, o Office 2013 

O Microsoft OLE DB Persistence Provider permite que você salve um objeto [Recordset](recordset-object-ado.md) em um arquivo e, posteriormente, restaure esse objeto **Recordset** a partir do arquivo. As informações do esquema, os dados e as alterações pendentes são preservados.

Você pode salvar o objeto **Recordset** usando o formato proprietário ADTG (Advanced Data Table Gram) ou o formato aberto XML (Extensible Markup Language).

## <a name="provider-keyword"></a>Palavra-chave do provedor

Para invocar esse provedor, especifique na sequência de conexão a palavra-chave e o valor abaixo.

```vb 
 
"Provider=MSPersist" 
```

## <a name="errors"></a>Erros

Os seguintes erros emitidos por esse provedor podem ser detectados no seu aplicativo:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>E_BADSTREAM</p></td>
<td><p>O arquivo aberto não tem um formato válido (ou seja, o formato não é ADTG ou XML).</p></td>
</tr>
<tr class="even">
<td><p>E_CANTPERSISTROWSET</p></td>
<td><p>O objeto <strong>Recordset</strong> que foi salvo possui características que impedem o seu armazenamento.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

O Microsoft OLE DB Persistence Provider não expõe qualquer propriedade dinâmica.

Atualmente, somente objetos **Recordset** hierárquicos com parâmetros não podem ser salvos.

Para obter mais informações sobre o armazenamento persistente de objetos **Recordset**, consulte [Persistência de Recordset](more-about-recordset-persistence.md).

Quando um fluxo é usado para abrir um **Recordset**, deve haver sem parâmetros especificado, exceto o parâmetro *Source* do método **Open** .

