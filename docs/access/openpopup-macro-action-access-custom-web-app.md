---
title: Ação de Macro OpenPopup (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 850de802-e417-4884-8d14-571de52aa391
description: Abre o modo de exibição especificado em uma janela pop-up.
ms.openlocfilehash: 01e0086dc0b54837cf5f095ec6ac5701b5b0b219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765198"
---
# <a name="openpopup-macro-action-access-custom-web-app"></a>Ação de Macro OpenPopup (aplicativo da web personalizado do Access)

Abre o modo de exibição especificado em uma janela pop-up.
  
> [!IMPORTANT]
> [!IMPORTANTE] A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Syntax

 **OpenPopup** (*Modo de exibição*, *onde =*, *Ordenar por*) 
  
A ação **OpenPopup** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *View*  <br/> |O nome da exibição a ser aberto.  <br/> |
| *Onde =*  <br/> |Uma cláusula SQL WHERE válida (sem a palavra onde) que restringe os registros no modo de exibição.  <br/> |
| *Classificado por*  <br/> |Uma expressão de cadeia de caracteres que inclui o nome do(s) campo(s) no(s) qual(is) serão classificados os registros e as palavras-chave CRESC ou DECRESC opcionais. Por padrão, esse argumento estiver em branco.  <br/> |
   
## <a name="remarks"></a>Coment�rios

A macro atual termina depois que a ação **OpenPopup** é processada. 
  
Qualquer classificação ou filtragem aplicada pelo usuário é limpa quando a ação **OpenPopup** é chamada. 
  
O argumento *OrderBy* é o nome do campo ou dos campos nos quais você deseja classificar os registros. Quando você usa mais de um nome de campo, separe-os com vírgula (,). 
  
Quando você define o argumento *OrderBy* , os registros são classificados por padrão em ordem crescente. 
  

