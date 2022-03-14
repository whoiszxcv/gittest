# gittest
<!-- Редактирование в группе элементов -->


for (let elem of elems) {
	elem.addEventListener('click', function func() {
		let input = document.createElement('input');
		input.value = elem.innerHTML;
		
		elem.innerHTML = '';
		elem.appendChild(input);
		
		input.addEventListener('blur', function() {
			elem.innerHTML = this.value;
			elem.addEventListener('click', func);
		});
		
		elem.removeEventListener('click', func);
	});
}
