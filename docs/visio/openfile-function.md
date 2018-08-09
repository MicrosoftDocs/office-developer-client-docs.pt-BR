---
title: Função OPENFILE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251471
localization_priority: Normal
ms.assetid: ff59ab04-a589-cf9e-db3b-20658a7dffdc
description: Abre um documento do Microsoft Visio, se não ainda estiver aberto e ativa a janela de documento.
ms.openlocfilehash: 7d4778fc4641465e88303b8515365172fd8be0ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772434"
---
# <a name="openfile-function"></a>Função OPENFILE

Abre um documento do Microsoft Visio, se não ainda estiver aberto e ativa a janela de documento.
  
## <a name="syntax"></a>Sintaxe

 **OPENFILE** ( _"filename"_)
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _FileName_ <br/> |Obrigatório  <br/> |**String** <br/> |O nome do arquivo, incluindo o caminho do arquivo que você deseja abrir.  <br/> |
   
## <a name="remarks"></a>Comentários

Chamadas múltiplas da função OPENFILE permanecem na fila e são executadas por ordem de avaliação. Se o documento atual do Visio estiver ativo para edição visual (in-loco), uma nova instância do Visio será inicializada com o nome de arquivo solicitado. 
  
Essa função sempre retornará FALSO. 
  
Em versões anteriores do aplicativo Visio, essa função aparece como _OPENFILE. As versões 4.0 e posteriores do Visio aceitam os dois estilos. 
  
## <a name="example"></a>Exemplo

 `OPENFILE("C:/MyFile.vsdx")`
  
Abre o arquivo especificado "MyFile.vsdx" em uma nova janela ou ativa a janela se o arquivo já está aberto. 
  

