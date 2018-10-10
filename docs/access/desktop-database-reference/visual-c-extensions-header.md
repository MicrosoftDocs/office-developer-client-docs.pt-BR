---
title: Cabeçalho de extensões do Visual C++
TOCTitle: Visual C++ Extensions Header
ms:assetid: 59fb9758-be43-051e-b3ae-6fdf50218057
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249308(v=office.15)
ms:contentKeyID: 48545032
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 78fc2a0b17637dcb0328995dcfc8b93edee2e326
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462000"
---
# <a name="visual-c-extensions-header"></a>Cabeçalho de extensões do Visual C++


**Aplica-se a**: Access 2013 | Office 2013

O cabeçalho a seguir, **icrsint.h**, detalha a interface que permite que clientes recuperem campos de um **Recordset** para as variáveis definidas em uma classe derivada de **CADORecordBinding**. Especifique uma macro de ligação ADO para cada campo que deseje acessar.

```cpp 
 
#ifndef _ICRSINT_H_ 
#define _ICRSINT_H_ 
 
#include <olectl.h> 
#include <stddef.h> 
 
// forwards 
class CADORecordBinding; 
 
#define classoffset(base, derived) ((DWORD)(static_cast<base*>((derived*)8))-8) 
 
enum ADOFieldStatusEnum 
{ 
 adFldOK = 0, 
 adFldBadAccessor = 1, 
 adFldCantConvertValue = 2, 
 adFldNull = 3, 
 adFldTruncated = 4, 
 adFldSignMismatch = 5, 
 adFldDataOverFlow = 6, 
 adFldCantCreate = 7, 
 adFldUnavailable = 8, 
 adFldPermissionDenied = 9, 
 adFldIntegrityViolation = 10, 
 adFldSchemaViolation = 11, 
 adFldBadStatus = 12, 
 adFldDefault = 13 
}; 
 
typedef struct stADO_BINDING_ENTRY 
{ 
 ULONG ulOrdinal; 
 WORD wDataType; 
 BYTE bPrecision; 
 BYTE bScale; 
 ULONG ulSize; 
 ULONG ulBufferOffset; 
 ULONG ulStatusOffset; 
 ULONG ulLengthOffset; 
 ULONG ulADORecordBindingOffSet; 
 BOOL fModify; 
} ADO_BINDING_ENTRY; 
 
#define BEGIN_ADO_BINDING(cls) public: typedef cls ADORowClass; const ADO_BINDING_ENTRY* STDMETHODCALLTYPE GetADOBindingEntries() { static const ADO_BINDING_ENTRY rgADOBindingEntries[] = { 
 
// 
// Fixed length non-numeric data 
// 
#define ADO_FIXED_LENGTH_ENTRY(Ordinal, DataType, Buffer, Status, Modify) {Ordinal, DataType, 0, 0, 0, offsetof(ADORowClass, Buffer), offsetof(ADORowClass, Status), 0, classoffset(CADORecordBinding, ADORowClass), Modify}, 
 
#define ADO_FIXED_LENGTH_ENTRY2(Ordinal, DataType, Buffer, Modify) {Ordinal, DataType, 0, 0, 0, offsetof(ADORowClass, Buffer), 0, 0, classoffset(CADORecordBinding, ADORowClass), Modify}, 
 
// 
// Numeric data 
// 
#define ADO_NUMERIC_ENTRY(Ordinal, DataType, Buffer, Precision, Scale, Status, Modify) {Ordinal, DataType, Precision, Scale, 0, offsetof(ADORowClass, Buffer), offsetof(ADORowClass, Status), 0, classoffset(CADORecordBinding, ADORowClass), Modify}, 
 
#define ADO_NUMERIC_ENTRY2(Ordinal, DataType, Buffer, Precision, Scale, Modify) {Ordinal, DataType, Precision, Scale, 0, offsetof(ADORowClass, Buffer), 0, 0, classoffset(CADORecordBinding, ADORowClass), Modify}, 
 
// 
// Variable length data 
// 
#define ADO_VARIABLE_LENGTH_ENTRY(Ordinal, DataType, Buffer, Size, Status, Length, Modify) {Ordinal, DataType, 0, 0, Size, offsetof(ADORowClass, Buffer), offsetof(ADORowClass, Status), offsetof(ADORowClass, Length), classoffset(CADORecordBinding, ADORowClass), Modify}, 
 
#define ADO_VARIABLE_LENGTH_ENTRY2(Ordinal, DataType, Buffer, Size, Status, Modify) {Ordinal, DataType, 0, 0, Size, offsetof(ADORowClass, Buffer), offsetof(ADORowClass, Status), 0, classoffset(CADORecordBinding, ADORowClass), Modify}, 
 
#define ADO_VARIABLE_LENGTH_ENTRY3(Ordinal, DataType, Buffer, Size, Length, Modify) {Ordinal, DataType, 0, 0, Size, offsetof(ADORowClass, Buffer), 0, offsetof(ADORowClass, Length), classoffset(CADORecordBinding, ADORowClass), Modify}, 
 
#define ADO_VARIABLE_LENGTH_ENTRY4(Ordinal, DataType, Buffer, Size, Modify) {Ordinal, DataType, 0, 0, Size, offsetof(ADORowClass, Buffer), 0, 0, classoffset(CADORecordBinding, ADORowClass), Modify}, 
 
#define END_ADO_BINDING() {0, adEmpty, 0, 0, 0, 0, 0, 0, 0, FALSE}}; return rgADOBindingEntries;} 
 
// 
// Interface that the client 'record' class needs to support. The ADO Binding entries 
// provide the implementation for this interface. 
// 
class CADORecordBinding 
{ 
public: 
 STDMETHOD_(const ADO_BINDING_ENTRY*, GetADOBindingEntries) (VOID) PURE; 
}; 
 
// 
// Interface that allows a client to fetch a record of data into class data members. 
// 
struct __declspec(uuid("00000544-0000-0010-8000-00aa006d2ea4")) IADORecordBinding; 
DECLARE_INTERFACE_(IADORecordBinding, IUnknown) 
{ 
public: 
 STDMETHOD(BindToRecordset) (CADORecordBinding *pAdoRecordBinding) PURE; 
 STDMETHOD(AddNew) (CADORecordBinding *pAdoRecordBinding) PURE; 
 STDMETHOD(Update) (CADORecordBinding *pAdoRecordBinding) PURE; 
}; 
 
#endif // !_ICRSINT_H_ 
```

