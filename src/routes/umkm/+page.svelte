<script>
	import { PUBLIC_CF_TURNSTILE_SITE_KEY } from '$env/static/public';
	import { Turnstile } from 'svelte-turnstile';

	/** @type {import('./$types').ActionData} */
	export let form;
</script>

{#if form?.error}
	<p class="error-message">{form?.error}</p>
{/if}

{#if form?.success}
	<script>
		window.alert('Kami sangat senang Anda telah menjadi bagian dari Pendataan UMKM Nasional.');
	</script>
{/if}

<svelte:head>
	<title>Mari Bersinergi, Sukseskan Pendataan UMKM demi Indonesia Maju!</title>
</svelte:head>
<!--  -->
<h1>Mari Bersinergi, Sukseskan Pendataan UMKM demi Indonesia Maju!</h1>
<p>Bersama Wujudkan UMKM Tangguh, Sukseskan Pendataan Nasional!</p>

<form method="POST">
	<label for="nama_pic">
		Nama Penanggung Jawab *)
		<input id="nama_pic" name="nama_pic" type="text" required />
	</label>
	<label for="nik">
		NIK *)
		<input id="nik" name="nik" type="number" required />
	</label>
	<label for="email">
		Email *)
		<input id="email" name="email" type="email" required />
	</label>
	<label for="telp">
		No Telp *)
		<input id="telp" name="telp" type="number" required />
	</label>
	<label for="alamat_pic">
		Alamat sesuai KTP *)
		<textarea id="alamat_pic" name="alamat_pic" required></textarea>
	</label>
	<label for="nama_usaha">
		Nama Perusahaan *)
		<input id="nama_usaha" name="nama_usaha" type="text" required />
	</label>
	<label for="alamat_usaha">
		Alamat Perusahaan *)
		<textarea id="alamat_usaha" name="alamat_usaha" required></textarea>
	</label>
	<label for="provinsi">
		Provinsi *)
		<select id="provinsi" name="provinsi" required>
			<option value="">Pilih provinsi</option>
			<option value="Aceh">Nanggroe Aceh Darussalam</option>
			<option value="Sumatera Utara">Sumatera Utara</option>
			<option value="Sumatera Selatan">Sumatera Selatan</option>
			<option value="Sumatera Barat">Sumatera Barat</option>
			<option value="Bengkulu">Bengkulu</option>
			<option value="Riau">Riau</option>
			<option value="Kepulauan Riau">Kepulauan Riau</option>
			<option value="Jambi">Jambi</option>
			<option value="Lampung">Lampung</option>
			<option value="Bangka Belitung">Bangka Belitung</option>
			<option value="Kalimantan Barat">Kalimantan Barat</option>
			<option value="Kalimantan Timur">Kalimantan Timur</option>
			<option value="Kalimantan Selatan">Kalimantan Selatan</option>
			<option value="Kalimantan Tengah">Kalimantan Tengah</option>
			<option value="Kalimantan Utara">Kalimantan Utara</option>
			<option value="Banten">Banten</option>
			<option value="DKI Jakarta">DKI Jakarta</option>
			<option value="Jawa Barat">Jawa Barat</option>
			<option value="Jawa Tengah">Jawa Tengah</option>
			<option value="Yogyakarta">Daerah Istimewa Yogyakarta</option>
			<option value="Jawa Timur">Jawa Timur</option>
			<option value="Bali">Bali</option>
			<option value="Nusa Tenggara Timur">Nusa Tenggara Timur</option>
			<option value="Nusa Tenggara Barat">Nusa Tenggara Barat</option>
			<option value="Gorontalo">Gorontalo</option>
			<option value="Sulawesi Barat">Sulawesi Barat</option>
			<option value="Sulawesi Tengah">Sulawesi Tengah</option>
			<option value="Sulawesi Utara">Sulawesi Utara</option>
			<option value="Sulawesi Tenggara">Sulawesi Tenggara</option>
			<option value="Sulawesi Selatan">Sulawesi Selatan</option>
			<option value="Maluku Utara">Maluku Utara</option>
			<option value="Maluku">Maluku</option>
			<option value="Papua Barat">Papua Barat</option>
			<option value="Papua">Papua</option>
			<option value="Papua Tengah">Papua Tengah</option>
			<option value="Papua Pegunungan">Papua Pegunungan</option>
			<option value="Papua Selatan">Papua Selatan</option>
			<option value="Papua Barat Daya">Papua Barat Daya</option>
		</select>
	</label>
	<label for="kab_kota">
		Kabupaten/Kota *)
		<input id="kab_kota" name="kab_kota" type="text" required />
	</label>
	<label for="kecamatan">
		Kecamatan *)
		<input id="kecamatan" name="kecamatan" type="text" required />
	</label>
	<label for="kodepos">
		Kodepos *)
		<input id="kodepos" name="kodepos" type="number" required />
	</label>
	<label for="list_kbli">
		Nomer KBLI (pisahkan dengan <strong>garis miring</strong>)
		<input id="list_kbli" name="list_kbli" type="text" />
	</label>
	<label for="kategori_usaha">
		Kategori Usaha *)
		<select id="kategori_usaha" name="kategori_usaha" required>
			<option value="">Pilih kategori usaha</option>
			<option value="UsahaIndustri">Usaha Industri</option>
			<option value="TreatmentAirWasteWater"
				>Treatment Air, Treatment Air Limbah, Treatment dan Pemulihan Material Sampah, dan Aktivitas
				Remediasi</option
			>
			<option value="RealEstate">Real Estate</option>
			<option value="PertanianKehutananPerikanan">Pertanian, Kehutanan dan Perikanan</option>
			<option value="PertambanganPenggalian">Pertambangan dan Penggalian</option>
			<option value="PerdaganganBesarEceran">Perdagangan Besar dan Eceran</option>
			<option value="AkomodasiMakanMinum">Penyediaan Akomodasi dan Penyediaan Makan Minum</option>
			<option value="PengangkutanPergudangan">Pengangkutan dan Pergudangan</option>
			<option value="ListrikGasUapAirPanasUdaraDingin"
				>Pengadaan Listrik, Gas, Uap/Air Panas dan Udara Dingin</option
			>
			<option value="Pendidikan">Pendidikan</option>
			<option value="Konstruksi">Konstruksi</option>
			<option value="KesenianHiburanRekreasi">Kesenian, Hiburan dan Rekreasi</option>
			<option value="InformasiKomunikasi">Informasi dan Komunikasi</option>
			<option value="IndustriPengolahan">Industri Pengolahan</option>
			<option value="AktivitasSosialTanpaAkomodasi">Aktivitas Sosial Tanpa Akomodasi</option>
			<option value="AktivitasProfesionalIlmiahTeknis"
				>Aktivitas Profesional, Ilmiah dan Teknis</option
			>
			<option value="PenyewaanSewaGunaUsaha"
				>Aktivitas Penyewaan dan Sewa Guna Usaha Tanpa Hak Opsi, Ketenagakerjaan, Agen Perjalanan
				dan Penunjang Usaha Lainnya</option
			>
			<option value="AktivitasKeuanganAsuransi">Aktivitas Keuangan dan Asuransi</option>
			<option value="AktivitasKesehatanManusiaAktivitasSosial"
				>Aktivitas Kesehatan Manusia dan Aktivitas Sosial</option
			>
			<option value="AktivitasJasaLainnya">Aktivitas Jasa Lainnya</option>
		</select>
	</label>
	<Turnstile siteKey={PUBLIC_CF_TURNSTILE_SITE_KEY} />
	<br />
	<div align="left">
		<input type="checkbox" id="consent" name="consent" required />
		<label for="consent">Saya setuju untuk membagikan data saya dengan formulir ini. *)</label>
	</div>
	<br />
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
