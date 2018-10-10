---
title: Wrappers da classe Java do ADO
TOCTitle: ADO Java Class Wrappers
ms:assetid: de50faf0-80f3-f295-3d9e-3f70f86c3ede
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250126(v=office.15)
ms:contentKeyID: 48548183
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fa3a4d1d2a917997b9e7ed5407d4f2ce8d1d0361
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464110"
---
# <a name="ado-java-class-wrappers"></a>Wrappers da classe Java do ADO


**Aplica-se a**: Access 2013 | Office 2013

Este código declara uma instância do wrapper da classe [Recordset](recordset-object-ado.md) do ADO e a inicializa, tudo na mesma linha de código. Além disso, ele declara variáveis para cada um dos argumentos no método [Open](open-method-ado-recordset.md), especialmente para [LockType](locktype-property-ado.md) e [CursorType](cursortype-property-ado.md) (pois o Java não oferece suporte a tipos enumerados). Ele abre e fecha o objeto **Recordset**. Definir Rs1 como NULL apenas faz com que esta variável seja lançada quando o Java executar o lançamento sistemático e intermitente de objetos não utilizados.

```java 
 
public static void main( String args[]) 
{ 
 msado15._Recordset Rs1 = new msado15.Recordset(); 
 Variant Source = new Variant( "SELECT * FROM Authors" ); 
 Variant Connect = new Variant( "DSN=AdoDemo;UID=admin;PWD=;" ); 
 int LockType = msado15.CursorTypeEnum.adOpenForwardOnly; 
 int CursorType = msado15.LockTypeEnum.adLockReadOnly; 
 int Options = -1; 
 
 Rs1.Open( Source, Connect, LockType, CursorType, Options ); 
 Rs1.Close(); 
 Rs1 = null; 
 
 System.out.println( "Success!\n" ); 
} 
```

