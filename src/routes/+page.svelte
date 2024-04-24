<script>
	import { PUBLIC_CF_TURNSTILE_SITE_KEY } from '$env/static/public';
	import { Turnstile } from 'svelte-turnstile';
</script>

{#if form?.error}
	<p class="error-message">{form?.error}</p>
{/if}

{#if form?.success}
	<script>
		window.alert('Kami sangat senang Anda telah menjadi bagian dari Pendataan UMKM Nasional.');
	</script>
{/if}

<!--  -->
<h1>Mari Bersinergi, Sukseskan Pendataan UMKM demi Indonesia Maju!</h1>
<p>Bersama Wujudkan UMKM Tangguh, Sukseskan Pendataan Nasional!</p>

<form method="POST">
	<label for="nama_pic">
		Nama Penanggung Jawab
		<input id="nama_pic" name="nama_pic" type="text" required />
	</label>
	<label for="nik">
		NIK
		<input id="nik" name="nik" type="number" required />
	</label>
	<label for="email">
		Email
		<input id="email" name="email" type="email" required />
	</label>
	<label for="telp">
		No Telp
		<input id="telp" name="telp" type="number" required />
	</label>
	<label for="alamat_pic">
		Alamat sesuai KTP
		<textarea id="alamat_pic" name="alamat_pic" required></textarea>
	</label>
	<label for="nama_usaha">
		Nama Penanggung Jawab
		<input id="nama_usaha" name="nama_usaha" type="text" required />
	</label>
	<label for="alamat_usaha">
		Alamat Perusahaan
		<textarea id="alamat_usaha" name="alamat_usaha" required></textarea>
	</label>
	<label for="provinsi">
		Provinsi
		<select id="provinsi" name="provinsi">
			<option value="">Please select a province</option>
			<option value="Aceh">Nanggroe Aceh Darussalam</option>
			<option value="SumateraUtara">Sumatera Utara</option>
			<option value="SumateraSelatan">Sumatera Selatan</option>
			<option value="SumateraBarat">Sumatera Barat</option>
			<option value="Bengkulu">Bengkulu</option>
			<option value="Riau">Riau</option>
			<option value="KepulauanRiau">Kepulauan Riau</option>
			<option value="Jambi">Jambi</option>
			<option value="Lampung">Lampung</option>
			<option value="BangkaBelitung">Bangka Belitung</option>
			<option value="KalimantanBarat">Kalimantan Barat</option>
			<option value="KalimantanTimur">Kalimantan Timur</option>
			<option value="KalimantanSelatan">Kalimantan Selatan</option>
			<option value="KalimantanTengah">Kalimantan Tengah</option>
			<option value="KalimantanUtara">Kalimantan Utara</option>
			<option value="Banten">Banten</option>
			<option value="DKIJakarta">DKI Jakarta</option>
			<option value="JawaBarat">Jawa Barat</option>
			<option value="JawaTengah">Jawa Tengah</option>
			<option value="Yogyakarta">Daerah Istimewa Yogyakarta</option>
			<option value="JawaTimur">Jawa Timur</option>
			<option value="Bali">Bali</option>
			<option value="NusaTenggaraTimur">Nusa Tenggara Timur</option>
			<option value="NusaTenggaraBarat">Nusa Tenggara Barat</option>
			<option value="Gorontalo">Gorontalo</option>
			<option value="SulawesiBarat">Sulawesi Barat</option>
			<option value="SulawesiTengah">Sulawesi Tengah</option>
			<option value="SulawesiUtara">Sulawesi Utara</option>
			<option value="SulawesiTenggara">Sulawesi Tenggara</option>
			<option value="SulawesiSelatan">Sulawesi Selatan</option>
			<option value="MalukuUtara">Maluku Utara</option>
			<option value="Maluku">Maluku</option>
			<option value="PapuaBarat">Papua Barat</option>
			<option value="Papua">Papua</option>
			<option value="PapuaTengah">Papua Tengah</option>
			<option value="PapuaPegunungan">Papua Pegunungan</option>
			<option value="PapuaSelatan">Papua Selatan</option>
			<option value="PapuaBaratDaya">Papua Barat Daya</option>
		</select>
	</label>
	<label for="kab_kota">
		Kabupaten/Kota
		<input id="kab_kota" name="kab_kota" type="text" required />
	</label>
	<label for="kecamatan">
		Kecamatan
		<input id="kecamatan" name="kecamatan" type="text" required />
	</label>
	<label for="kodepos">
		Kodepos
		<input id="kodepos" name="kodepos" type="number" required />
	</label>
	<label for="list_kbli">
		Nomer KBLI (pisahkan dengan koma)
		<input id="list_kbli" name="list_kbli" type="text" required />
	</label>
	<label for="kategori">
		Kategori Usaha
		<input id="kategori" name="kategori" type="text" required />
	</label>
	<Turnstile siteKey={PUBLIC_CF_TURNSTILE_SITE_KEY} />
	<button type="submit">Kirim</button>
</form>

<style>
	form {
		max-width: 500px;
		margin: 0 auto;
		padding: 20px;
		border: 1px solid #ddd;
		border-radius: 8px;
		background: #f9f9f9;
	}
	h1 {
		text-align: center;
		color: #333;
	}
	p {
		text-align: center;
		color: #666;
	}
	label {
		display: block;
		margin-top: 20px;
		color: #333;
	}
	input,
	textarea {
		width: 100%;
		padding: 10px;
		margin-top: 5px;
		border: 1px solid #ccc;
		border-radius: 4px;
	}
	button {
		display: block;
		width: 100%;
		padding: 10px;
		margin-top: 20px;
		background-color: #0056b3;
		color: white;
		border: none;
		border-radius: 4px;
		cursor: pointer;
	}
	button:hover {
		background-color: #003d82;
	}
</style>
