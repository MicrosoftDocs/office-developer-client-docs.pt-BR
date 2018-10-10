---
title: Configurando o DCOM Stream Marshaling Format
TOCTitle: Setting DCOM Stream Marshaling Format
ms:assetid: 5f75fc59-a9f8-6686-07f9-de292e4da787
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249346(v=office.15)
ms:contentKeyID: 48545162
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c0c05a378624f118f1bf6f070273b686a2e50a6e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463755"
---
# <a name="setting-dcom-stream-marshaling-format"></a>Configurando o DCOM Stream Marshaling Format


**Aplica-se a**: Access 2013 | Office 2013

Um computador cliente que está usando componentes do RDS 1.5 ou anterior não é compatível com um servidor que está usando os componentes do RDS 2.0 ou posterior. Ao usar o DCOM como protocolo subjacente, o suporte para RDS 2.0 ou posterior é mais eficiente no transporte dos objetos [Recordset](recordset-object-ado.md). Se seu cliente estiver executando componentes do RDS 1.5 ou anterior, você poderá definir o servidor para trabalhar com o suporte ao RDS anterior (chamado RDS 1.0) ou o suporte ao RDS mais recente (chamado RDS 2.0 ou posterior). Defina uma das seguintes entradas de registro:

```vb 
 
[HKEY_CLASSES_ROOT] 
\CLSID 
 \[58ECEE30-E715-11CF-B0E3-00AA003F000F} 
 \ADTGOptions]"MarshalFormat"="RDS10" 
```

\-ou -

```vb 
 
[HKEY_CLASSES_ROOT] 
\CLSID 
 \[58ECEE30-E715-11CF-B0E3-00AA003F000F} 
 \ADTGOptions]"MarshalFormat"="RDS20" 
```

