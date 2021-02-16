---
title: Ação de macro AbrirPopup (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 850de802-e417-4884-8d14-571de52aa391
description: Abre o exibição especificado em uma janela pop-up.
ms.openlocfilehash: 2a8b67fcbf31c42f13b36f06d14d9d046be68c68
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427385"
---
# <a name="openpopup-macro-action-access-custom-web-app"></a>Ação de macro AbrirPopup (aplicativo Web personalizado do Access)

Abre o exibição especificado em uma janela pop-up.
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Sintaxe

 **OpenPopup** (*View*, *Where=*, *Order By*) 
  
A **ação AbrirPopup** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *View*  <br/> |O nome do modo de exibição que será aberto.  <br/> |
| *Where=*  <br/> |Uma cláusula SQL WHERE válida (sem a palavra WHERE) que restringe os registros no exibição.  <br/> |
| *Classificado Por*  <br/> |Uma expressão de cadeia de caracteres que inclui o nome do(s) campo(s) no(s) qual(is) serão classificados os registros e as palavras-chave CRESC ou DECRESC opcionais. Por padrão, esse argumento fica em branco.  <br/> |
   
## <a name="remarks"></a>Comentários

A macro atual termina depois que **a ação AbrirPopup** é processada. 
  
Qualquer classificação ou filtragem aplicada pelo usuário é limpa quando a **ação AbrirPopup** é chamada. 
  
O  *argumento OrderBy*  é o nome do campo ou dos campos nos quais você deseja classificar registros. Quando você usa mais de um nome de campo, separe-os com uma vírgula (,). 
  
Quando você definir o  *argumento OrderBy,*  os registros serão organizados por padrão em ordem crescente. 
  

