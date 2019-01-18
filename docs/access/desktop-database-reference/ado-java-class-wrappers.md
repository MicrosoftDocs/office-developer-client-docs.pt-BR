---
title: Wrappers da classe Java do ADO
TOCTitle: ADO Java class wrappers
ms:assetid: de50faf0-80f3-f295-3d9e-3f70f86c3ede
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250126(v=office.15)
ms:contentKeyID: 48548183
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 731e659f29d6fd504bab772867fb438985189e13
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704144"
---
# <a name="ado-java-class-wrappers"></a><span data-ttu-id="80f77-102">Wrappers da classe Java do ADO</span><span class="sxs-lookup"><span data-stu-id="80f77-102">ADO Java class wrappers</span></span>


<span data-ttu-id="80f77-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="80f77-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="80f77-p101">Este código declara uma instância do wrapper da classe [Recordset](recordset-object-ado.md) do ADO e a inicializa, tudo na mesma linha de código. Além disso, ele declara variáveis para cada um dos argumentos no método [Open](open-method-ado-recordset.md), especialmente para [LockType](locktype-property-ado.md) e [CursorType](cursortype-property-ado.md) (pois o Java não oferece suporte a tipos enumerados). Ele abre e fecha o objeto **Recordset**. Definir Rs1 como NULL apenas faz com que esta variável seja lançada quando o Java executar o lançamento sistemático e intermitente de objetos não utilizados.</span><span class="sxs-lookup"><span data-stu-id="80f77-p101">This code declares an instance of the ADO [Recordset](recordset-object-ado.md) class wrapper and initializes it, all on the same line of code. Further, it declares variables for each of the arguments in the [Open](open-method-ado-recordset.md) method, especially for [LockType](locktype-property-ado.md) and [CursorType](cursortype-property-ado.md) (because Java doesn't support enumerated types). It opens and closes the **Recordset** object. Setting Rs1 to NULL merely schedules that variable to be released when Java performs its systematic and intermittent release of unused objects.</span></span>

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

