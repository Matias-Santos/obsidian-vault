```js

function createItem(src) {
	const imgElement = 
}

imageInput.AddEventListener('change', (event) => {
	const [file = event.target.files
	
	if (files) = 

})

const rows = $$('.tier .row')

rows.forEach(row => {
	row.addEventListener('drop', handleDrop)
	row.addEventListener("dragOver", handleDragOver)
	row.addEventListener('drageLeave', handleDrageLeave)
})
	
	itemsSection.addEventListener('drop', handleDrop)
	itemsSection.addEventListener("dragOver", handleDragOver)
	itemsSection.addEventListener('drageLeave', handleDrageLeave)

function handleDrop() {
	event.preventDefault()
	
	const { currentTarget, dataTransfer } = event
	
	if ( sourceContainer && draggedElement) {
		sourceConteiner.revmoveChild(draggedElement)
	}
	
	if (draggedElement){
		const src = dataTransfer()
		const imgElement = ceateItem()
		currentTarget.appendChild(imgElement)
	}
	
	currentTarget.classList.remove('dragOver')
}

function handleDragOver(event) {
	event.preventDefault()
	
	if (sourceContainer === currentTarget) return
	const { currentTarget, dataTransfer } = event
	
	currentTarget.classList.add('dragOver')
}

function handleDragLeave(event) {
	event.preventDefault()
	
	const { currentTarget, dataTransfer } = event
	
	currentTarget.classList.remove('dragOver')
}

imageInput.draggable = true
function handleDragStart(event) {
	draggedElement = event.target
	
	const sourceContainer = draggedElement.parentNode
	
	event.dataTransfer.setData('text/plain', draggedElement.src)
}

function handleDragend(event) {
	draggedElement = null
	const sourceContainer = null
}
```